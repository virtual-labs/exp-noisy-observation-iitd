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

### Theory of Wiener Filtering

Wiener filtering is a fundamental technique in statistical signal processing used to estimate a desired signal from a noisy observation. The objective is to design a linear time-invariant (LTI) filter whose output minimizes the mean-square error (MSE) between the estimated signal and the desired signal.



### Signal Model and Notation

Let:

- $x[n]$ denote the observed (input) signal  
- $d[n]$ denote the desired (reference) signal  
- $h[n]$ denote the impulse response (filter coefficients)  
- $y[n]$ denote the filter output (estimate of $d[n]$)  
- $e[n]$ denote the estimation error  

The output of the LTI filter is given by the convolution:

$$
y[n] = \sum_{m=-\infty}^{\infty} h[m]\,x[n-m]
$$

Here, $h[m]$ represents the filter coefficient at lag $m$, and $x[n-m]$ is the input sample delayed by $m$. The summation combines all weighted past and future samples (for the general case).

The estimation error is defined as:

$$
e[n] = d[n] - y[n]
$$

This represents the difference between the desired signal and its estimate.



### Mean-Square Error Criterion

The performance of the filter is evaluated using the mean-square error:

$$
\xi = E\{e^2[n]\} = E\{(d[n] - y[n])^2\}
$$

Here, $E\{\cdot\}$ denotes the statistical expectation operator. The squaring ensures that both positive and negative errors contribute positively.

The Wiener filtering problem consists of determining the impulse response $h[n]$ that minimizes $\xi$:

$$
h_{\text{opt}} = \arg \min_h E\{(d[n] - y[n])^2\}
$$

Here, $\arg \min$ denotes the value of $h[n]$ that minimizes the MSE.



### Correlation Functions

#### Autocorrelation Function

The autocorrelation of the input signal is defined as:

$$
\varphi_{xx}[k] = E\{x[n]\,x[n+k]\}
$$

Here, $k$ is the lag (time shift). This function measures how similar the signal is to a shifted version of itself.

For wide-sense stationary (WSS) processes, $\varphi_{xx}[k]$ depends only on $k$.  
At $k=0$, $\varphi_{xx}[0] = E\{x^2[n]\}$ represents the average power of the input signal.

#### Cross-Correlation Function

The cross-correlation between the input and desired signal is:

$$
\varphi_{xd}[k] = E\{x[n]\,d[n+k]\}
$$

This measures how the input signal $x[n]$ is related to the desired signal $d[n]$ at a shift of $k$.



### Wiener–Hopf Equation

Minimization of the MSE leads to the Wiener–Hopf equation:

$$
\sum_{m=-\infty}^{\infty} h_{\text{opt}}[m]\,\varphi_{xx}[k-m] = \varphi_{xd}[k], \quad \forall k
$$

Here, $h_{\text{opt}}[m]$ are the optimal filter coefficients.  
This equation expresses that the filtered input must match the cross-correlation with the desired signal for all lags $k$.



### Frequency-Domain Representation

Taking the Fourier (or $z$-) transform of the Wiener–Hopf equation yields:

$$
H_{\text{opt}}(z) = \frac{\Phi_{xd}(z)}{\Phi_{xx}(z)}
$$

where:

- $\Phi_{xx}(z)$ is the power spectral density (PSD) of $x[n]$  
- $\Phi_{xd}(z)$ is the cross-power spectral density between $x[n]$ and $d[n]$  

Here, $H_{\text{opt}}(z)$ represents the frequency response of the optimal filter.



### Noise Reduction Model

Consider the additive noise model:

$$
x[n] = s[n] + v[n]
$$

where:
- $s[n]$ is the desired (clean) signal  
- $v[n]$ is additive noise  

Assume that $s[n]$ and $v[n]$ are uncorrelated, and let $d[n] = s[n]$. Then:

$$
\Phi_{xx}(z) = \Phi_{ss}(z) + \Phi_{vv}(z), \quad \Phi_{xd}(z) = \Phi_{ss}(z)
$$

Here:
- $\Phi_{ss}(z)$ is the PSD of the signal  
- $\Phi_{vv}(z)$ is the PSD of the noise  

The optimal Wiener filter becomes:

$$
H_{\text{opt}}(z) = \frac{\Phi_{ss}(z)}{\Phi_{ss}(z) + \Phi_{vv}(z)}
$$
At frequencies where the noise power $\Phi_{vv}(z)$ is large, the denominator increases, causing the filter to reduce the gain (attenuation) at those frequencies.



### Finite-Length (FIR) Wiener Filter

In practical implementations, a finite impulse response (FIR) filter of order $N$ is used:

$$
y[n] = \sum_{k=0}^{N-1} h[k]\,x[n-k]
$$

Here, only past and present samples are used, making the filter causal.

Define the coefficient vector and input vector as:

$$
H = [h[0], h[1], \dots, h[N-1]]^T
$$

$$
X[n] = [x[n], x[n-1], \dots, x[n-N+1]]^T
$$

Then the filter output is:

$$
y[n] = H^T X[n]
$$

Here, $H^T$ denotes the transpose of $H$, and the expression represents an inner product.

Define:

- $R = E\{X[n] X^T[n]\}$ : autocorrelation matrix of the input  
- $P = E\{X[n] d[n]\}$ : cross-correlation vector  

The optimal coefficient vector is obtained as:

$$
H_{\text{opt}} = R^{-1} P
$$
- **$R^{-1}$:** The inverse of the input autocorrelation matrix. It effectively "undoes" redundancies in the input data to help the filter isolate the unique parts of the signal.
- **$P$:** The cross-correlation vector. It indicates the direction in which the filter should adjust its weights to match the desired output.


### Minimum Mean-Square Error

The minimum achievable MSE is given by:

$$
\xi_{\min} = \sigma_d^2 - P^T R^{-1} P
$$

where:

$$
\sigma_d^2 = E\{d^2[n]\}
$$

Here, $d[n]$ denotes the desired signal, and $\sigma_d^2$ represents its average power.  
The term $P^T R^{-1} P$ represents the amount of the desired signal power that can be recovered (estimated) from the observed input signal $x[n]$.



### Applications

Wiener filtering is widely applied in:

- **Noise Reduction:** Removing background hiss from recordings.  
- **System Identification:** Mapping how an unknown system behaves.  
- **Channel Equalization:** Fixing distorted signals in 4G/5G networks.  
- **Image Restoration:** Removing "blur" from digital photographs.