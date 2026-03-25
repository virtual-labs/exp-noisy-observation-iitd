<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Wiener Filtering Theory</title>
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$','$$'], ['\\[','\\]']]
    },
    options: {
      skipHtmlTags: ['script', 'noscript', 'style', 'textarea', 'pre']
    }
  };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>
<body>

<h3>Theory of Wiener Filtering</h3>

<p>Wiener filtering is a fundamental technique in statistical signal processing used to estimate a desired signal from a noisy observation. The objective is to design a linear time-invariant (LTI) filter whose output minimizes the mean-square error (MSE) between the estimated signal and the desired signal.</p>

<h3>Signal Model and Notation</h3>
<ul>
  <li><strong>x[n]</strong> denote the observed (input) signal</li>
  <li><strong>d[n]</strong> denote the desired (reference) signal</li>
  <li><strong>h[n]</strong> denote the impulse response (filter coefficients)</li>
  <li><strong>y[n]</strong> denote the filter output (estimate of d[n])</li>
  <li><strong>e[n]</strong> denote the estimation error</li>
</ul>

<p>The output of the LTI filter is given by the convolution:</p>
$$
y[n] = \sum_{m=-\infty}^{\infty} h[m]\,x[n-m]
$$
<p>Here, h[m] represents the filter coefficient at lag m, and x[n-m] is the input sample delayed by m. The summation combines all weighted past and future samples (for the general case).</p>

<p>The estimation error is defined as:</p>
$$
e[n] = d[n] - y[n]
$$
<p>This represents the difference between the desired signal and its estimate.</p>

<h3>Mean-Square Error Criterion</h3>
<p>The performance of the filter is evaluated using the mean-square error:</p>
$$
\xi = E\{e^2[n]\} = E\{(d[n] - y[n])^2\}
$$
<p>Here, E{⋅} denotes the statistical expectation operator. The squaring ensures that both positive and negative errors contribute positively.</p>

<p>The Wiener filtering problem consists of determining the impulse response h[n] that minimizes ξ:</p>
$$
h_{\text{opt}} = \arg \min_h E\{(d[n] - y[n])^2\}
$$
<p>Here, <strong>arg min</strong> denotes the value of h[n] that minimizes the MSE.</p>

<h3>Correlation Functions</h3>

<h4>Autocorrelation Function</h4>
$$
\varphi_{xx}[k] = E\{x[n]\,x[n+k]\}
$$
<p>Here, k is the lag (time shift). This function measures how similar the signal is to a shifted version of itself.</p>
<p>For wide-sense stationary (WSS) processes, φxx[k] depends only on k. At k = 0, φxx[0] = E{x²[n]} represents the average power of the input signal.</p>

<h4>Cross-Correlation Function</h4>
$$
\varphi_{xd}[k] = E\{x[n]\,d[n+k]\}
$$
<p>This measures how the input signal x[n] is related to the desired signal d[n] at a shift of k.</p>

<h3>Wiener–Hopf Equation</h3>
$$
\sum_{m=-\infty}^{\infty} h_{\text{opt}}[m]\,\varphi_{xx}[k-m] = \varphi_{xd}[k], \quad \forall k
$$
<p>Here, h<sub>opt</sub>[m] are the optimal filter coefficients. This equation expresses that the filtered input must match the cross-correlation with the desired signal for all lags k.</p>

<h3>Frequency-Domain Representation</h3>
$$
H_{\text{opt}}(z) = \frac{\Phi_{xd}(z)}{\Phi_{xx}(z)}
$$
<ul>
  <li>Φxx(z) is the power spectral density (PSD) of x[n]</li>
  <li>Φxd(z) is the cross-power spectral density between x[n] and d[n]</li>
</ul>
<p>Here, H<sub>opt</sub>(z) represents the frequency response of the optimal filter.</p>

<h3>Noise Reduction Model</h3>
$$
x[n] = s[n] + v[n]
$$
<ul>
  <li>s[n] is the desired (clean) signal</li>
  <li>v[n] is additive noise</li>
</ul>
<p>Assume s[n] and v[n] are uncorrelated, and let d[n] = s[n]. Then:</p>
$$
\Phi_{xx}(z) = \Phi_{ss}(z) + \Phi_{vv}(z), \quad \Phi_{xd}(z) = \Phi_{ss}(z)
$$
<p>The optimal Wiener filter becomes:</p>
$$
H_{\text{opt}}(z) = \frac{\Phi_{ss}(z)}{\Phi_{ss}(z) + \Phi_{vv}(z)}
$$
<p>At frequencies where the noise power Φ<sub>vv</sub>(z) is large, the denominator increases, causing the filter to reduce the gain (attenuation) at those frequencies.</p>

<h3>Finite-Length (FIR) Wiener Filter</h3>
$$
y[n] = \sum_{k=0}^{N-1} h[k]\,x[n-k]
$$
<p>Here, only past and present samples are used, making the filter causal.</p>

<p>Define the coefficient vector and input vector:</p>
$$
H = [h[0], h[1], \dots, h[N-1]]^T
$$
$$
X[n] = [x[n], x[n-1], \dots, x[n-N+1]]^T
$$
<p>Then the filter output is:</p>
$$
y[n] = H^T X[n]
$$
<p>Here, H^T denotes the transpose of H, representing an inner product.</p>

<ul>
  <li>R = E{X[n] X^T[n]} : autocorrelation matrix of the input</li>
  <li>P = E{X[n] d[n]} : cross-correlation vector</li>
</ul>

$$
H_{\text{opt}} = R^{-1} P
$$
<ul>
  <li><strong>R<sup>-1</sup></strong>: The inverse of the input autocorrelation matrix. It helps the filter isolate the unique parts of the signal.</li>
  <li><strong>P</strong>: The cross-correlation vector. It indicates how the filter weights should be adjusted to match the desired output.</li>
</ul>

<h3>Minimum Mean-Square Error</h3>
$$
\xi_{\min} = \sigma_d^2 - P^T R^{-1} P
$$
$$
\sigma_d^2 = E\{d^2[n]\}
$$
<p>Here, d[n] denotes the desired signal, and σ<sub>d</sub>² represents its average power. The term P<sup>T</sup> R<sup>-1</sup> P represents the amount of the desired signal power that can be recovered (estimated) from the observed input signal x[n].</p>

<h3>Applications</h3>
<ul>
  <li><strong>Noise Reduction:</strong> Removing background hiss from recordings.</li>
  <li><strong>System Identification:</strong> Mapping how an unknown system behaves.</li>
  <li><strong>Channel Equalization:</strong> Fixing distorted signals in 4G/5G networks.</li>
  <li><strong>Image Restoration:</strong> Removing "blur" from digital photographs.</li>
</ul>

</body>
</html>
