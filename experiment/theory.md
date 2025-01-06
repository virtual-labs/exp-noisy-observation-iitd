<!DOCTYPE html>
<html lang="en-IN">
	<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<meta charset="utf-8" />
		<title>
		</title>
		<style>
			body { line-height:108%; font-family:Calibri; font-size:11pt }
			p { margin:0pt 0pt 8pt }
			li { margin-top:0pt; margin-bottom:8pt }
			.ListParagraph { margin-left:36pt; margin-bottom:8pt; line-height:108%; font-size:11pt }
@media (max-width: 900px) { 
img { 
   max-width: 100%;
   height: auto;
}

.table-container {
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
}

table {
    width: 100%;
    border-collapse: collapse;
}

td, th {
    padding: 8px;
    text-align: left;
    border: 1px solid #ddd;
}
}	


		</style>
	</head>
	<body>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Assuming known stationary signal and noise spectra and additive noise, the Wiener filter is a filter used in signal processing to provide an estimate of a desired or target random process through linear time-invariant (LTI) filtering of an observed noisy process. The mean square error between the intended process and the estimated random process is reduced by the Wiener filter.</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-1.png" width="348" height="100" alt="" />
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<strong><span style="font-family:'Times New Roman'; ">Fig: Block diagram view of the FIR Wiener filter for discrete series. An input signal x[n] is convolved with the Wiener filter g[n] and the result is compared to a reference signal s[n] to obtain the filtering error e[n].</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In the big picture, the signal is attenuated and added with noise, then the signal is passed through a Wiener filter. And the function of the Wiener filter is to minimize the mean square error between the filter output of the received signal and the reference signal by adjusting the Wiener filter tap coefficient.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">Description</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">By employing a related signal as an input and filtering that known signal to obtain the estimate as an output, the Wiener filter aims to compute a statistical estimate of an unknown signal. For instance, the known signal might be made up of a potentially valuable unknown signal that has been tampered with by additive noise. By removing the noise from the distorted signal, the Wiener filter can estimate the underlying signal of interest. The Wiener filter is based on a statistical methodology, and the article on the minimum mean square error (MMSE) estimator provides a more statistical explanation of the theory. Here x[n] is a wide-sense stationary (WSS) random process that we have measurements of. We want to determine the unit sample response or frequency response of the above LTI system such that the filter output y</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">[n] is the minimum-mean-square-error (MMSE) estimate of some “target” process y[n] that is jointly WSS with x[n]. Defining the error e[n] as</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-2.png" width="185" height="47" alt="" />
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">we wish to carry out the following minimization:</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-3.png" width="184" height="42" alt="" />
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The resulting filter h[n] is called the Wiener filter for the estimation of y[n] from x[n]. In some contexts it is appropriate or convenient to restrict the filter to be an FIR (finite-duration impulse response) filter of length N, e.g. h[n] = 0 except in the interval 0 ≤ n ≤ N − 1.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The Wiener filter seeks to generate a statistical estimate of an unknown signal by using a related signal as an input and filtering that known signal to produce the estimate as an output. As an illustration, the known signal can consist of an unknown signal that is potentially valuable but has been tampered with by additive noise. The Wiener filter can estimate the underlying signal of interest by eliminating the noise from the distorted signal. The article on the minimal mean square error (MMSE) estimator offers a more statistical justification of the theory because the Wiener filter is based on a statistical technique.</span>
			</p>
			<ol style="margin:0pt; padding-left:0pt">
				<li class="ListParagraph" style="margin-left:33.5pt; margin-bottom:0pt; text-align:justify; line-height:108%; padding-left:2.5pt; font-family:'Times New Roman'; font-size:14pt">
					Assumption: signal and (additive) noise are stationary linear stochastic processes with known spectral characteristics or known autocorrelation and cross-correlation
				</li>
				<li class="ListParagraph" style="margin-left:33.5pt; margin-bottom:0pt; text-align:justify; line-height:108%; padding-left:2.5pt; font-family:'Times New Roman'; font-size:14pt">
					Requirement: the filter must be physically realizable/causal (this requirement can be dropped, resulting in a non-causal solution)
				</li>
				<li class="ListParagraph" style="margin-left:33.5pt; text-align:justify; line-height:108%; padding-left:2.5pt; font-family:'Times New Roman'; font-size:14pt">
					Performance criterion: minimum mean-square error (MMSE)
				</li>
			</ol>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">This filter is frequently used in the process of deconvolution; for this application, see Wiener deconvolution.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-4.png" width="535" height="104" alt="" />
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Fig: DT LTI filter for linear MMSE estimation</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">Non-causal DT Wiener Filter</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">To determine the optimal choice for h[n], we first expand the error criterion in</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-5.png" width="410" height="76" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (i)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The impulse response values that minimize ϵ can then be obtained by setting</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">∂ϵ/∂h[m] = 0 for all values of m for which h[m] is not restricted to be zero (or ∂h[m] otherwise pre-specified):</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-6.png" width="461" height="109" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (ii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The above equation implies that</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">E{e[n]x[n-m]} = 0</span><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (iii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Or, R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>ex</sub></span><span style="font-family:'Times New Roman'">[m] = 0, for all m for which h[m] can be freely chosen.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>ex</sub></span><span style="font-family:'Times New Roman'">[m] = E{e[n]x[n-m]}</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">= E{(y</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">[n] - y[n])x[n-m]}</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span><em><span style="font-family:'Times New Roman'; ">[y</span></em><em><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span></em><em><span style="font-family:'Times New Roman'; ">[n] is the estimated received signal]</span></em>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">= R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>y</sub></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>x</sub></span><span style="font-family:'Times New Roman'">[m] - R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">[m]</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (iv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Or,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>y</sub></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>x</sub></span><span style="font-family:'Times New Roman'">[m] - R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">[m] = 0</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Therefore, an alternative way of stating the orthogonality principle in equation (iv) from equation (iii) is that </span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>y</sub></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>x</sub></span><span style="font-family:'Times New Roman'">[m] = R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">[m]</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">for all appropriate m</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<em><span style="font-family:'Times New Roman'; ">[R</span></em><em><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span></em><em><span style="font-family:'Times New Roman'; "> is the cross-correlation between the output of the wiener filter y and input x]</span></em>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In other words, for the optimal system, the cross-correlation between the input and output of the estimator equals the cross-correlation between the input and target output.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">To actually find the impulse response values, observe that since y</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">[n] is obtained by filtering x[n] through an LTI system with impulse response h[n], the following relationship applies:</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-7.png" width="253" height="35" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (v)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Combining this with the alternative statement of the orthogonality condition, we</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">can write</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-8.png" width="258" height="45" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (vi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Or, equivalently, </span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-9.png" width="314" height="65" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (vii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Equation (vii) represents a set of linear equations to be solved for the impulse</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">response values. If the filter is FIR of length N, then there are N equations in the</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">N unrestricted values of h[n]. For instance, suppose that h[n] is restricted to be</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">zero except for n </span><span style="font-family:'Cambria Math'">∈</span><span style="font-family:'Times New Roman'"> [0, N −1]. The condition then yields as many equations as unknowns, which can be arranged in the following matrix form, which you may recognize as the appropriate form of the normal equations for LMMSE estimation</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-10.png" width="438" height="98" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">…(viii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In the case of an IIR filter, equation (vii) must hold for an infinite number of values of m and, therefore, cannot simply be solved by the methods used for a finite number of linear equations. However, if h[n] is not restricted to be causal or FIR, the equation must hold for all values of m from −∞ to +∞, so the z-transform can be applied to equation to obtain</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-11.png" width="221" height="30" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (ix)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The optimal transfer function, i.e. the transfer function of the resulting (Wiener)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">filter, is then</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-12.png" width="237" height="29" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (x)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">If either of the correlation functions involved in this calculation does not possess a z-transform but if both possess Fourier transforms, then the calculation can be carried out in the Fourier transform domain.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Similarly in continuous time results are exactly the same</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-13.png" width="179" height="31" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-14.png" width="246" height="31" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-15.png" width="216" height="27" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xiii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-16.png" width="230" height="25" alt="" /><span style="font-family:'Times New Roman'"> … (xiv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The mean-square-error corresponding to the optimum filter, i.e. the minimum</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">MSE, can be determined by straightforward computation. We leave you to show</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">That</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-17.png" width="515" height="28" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">where h[m] is the impulse response of the optimal filter. The MMSE is then just</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>ee</sub></span><span style="font-family:'Times New Roman'">[0]. It is illuminating to rewrite this in the frequency domain, but dropping the argument e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ </sup></span><span style="font-family:'Times New Roman'">on the power spectra S(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'">) and frequency response H(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'"> ) below to avoid notational clutter:</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-18.png" width="441" height="199" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xvi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The function ρ</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'">) defined by</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-19.png" width="315" height="55" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xvii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Consider a situation in which x[n], the sum of a target process y[n] and noise v[n], is observed:</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We would like to estimate y[n] from our observations of x[n]. Assume that the signal and noise are uncorrelated, i.e. R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vy</sub></span><span style="font-family:'Times New Roman'">[m] = 0. Then</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">x[n] = y[n] + v[n]</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xviii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We would like to estimate y[n] from our observations of x[n]. Assume that the</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">signal and noise are uncorrelated, i.e. R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vy</sub></span><span style="font-family:'Times New Roman'">[m] = 0. Then</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">[m] = R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yy</sub></span><span style="font-family:'Times New Roman'">[m] + R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vv</sub></span><span style="font-family:'Times New Roman'">[m]</span><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xix)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">[m] = R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yy</sub></span><span style="font-family:'Times New Roman'">[m]</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xx)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-20.png" width="302" height="45" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">At values of Ω for which the signal power is much greater than the noise power,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">H(ejΩ) ≈ 1. Where the noise power is much greater than the signal power,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">H(ejΩ) ≈ 0. For example, when</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-21.png" width="475" height="33" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">and the noise is white, the optimal filter will be a low-pass filter with a frequency response that is appropriately shaped, shown in Figure below. Note that the filter in</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-22.png" width="602" height="264" alt="" />
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Fig: Optimal filter frequency response, H(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'">), input signal PSD signal,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yy</sub></span><span style="font-family:'Times New Roman'">(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'">), and PSD of white noise, S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vv</sub></span><span style="font-family:'Times New Roman'">(e</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>jΩ</sup></span><span style="font-family:'Times New Roman'">).</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-23.png" width="602" height="108" alt="" />
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In the Figure 11.4, r[n] is a filtered or “blurred” version of the signal of interest,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">x[n], while v[n] is additive noise that is uncorrelated with x[n]. We wish to design a filter that will deblur the noisy measured signal ξ[n] and produce an estimate of the input signal x[n]. Note that in the absence of the additive noise, the inverse filter 1/G(z) will recover the input exactly. However, this is not a good solution when noise is present, because the inverse filter accentuates precisely those frequencies where the measurement power is small relative to that of the noise. We shall therefore design a Wiener filter to produce an estimate of the signal x[n].</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We have shown that the cross-correlation between the measured signal, which is the input to the Wiener filter, and the estimate produced at its output is equal to the cross-correlation between the measurement process and the target process. In the transform domain, the statement of this condition is</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-24.png" width="177" height="36" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxiii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Or,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-25.png" width="315" height="40" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxiv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We also know that,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>ξ ξ </sub></span><span style="font-family:'Times New Roman'">(z) = S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vv</sub></span><span style="font-family:'Times New Roman'">(z) + S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(z)G(z)G(1/z)</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xꜪ </sub></span><span style="font-family:'Times New Roman'">(z) = S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xr </sub></span><span style="font-family:'Times New Roman'">(z) … (xxvi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">= S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx </sub></span><span style="font-family:'Times New Roman'">(z) G(1/z)</span><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxvii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">where we have (in the first equality above) used the fact that </span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vr</sub></span><span style="font-family:'Times New Roman'">(z) = G(1/z)S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>vx</sub></span><span style="font-family:'Times New Roman'">(z) = 0. We can now write</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-26.png" width="377" height="58" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxviii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We leave you to check that this system function assumes reasonable values in the limiting cases where the noise power is very small, or very large. It is also interesting to verify that the same overall filter is obtained if we first find an MMSE estimate r</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">[n] from ξ[n] (as in Example </span><img src="1736155213_wiener-filter/1736155213_wiener-filter-27.png" width="186" height="22" alt="" /><span style="font-family:'Times New Roman'">), and then pass r</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">[n] through the inverse filter 1/G(z).</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">&#xa0;</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">Non-causal CT Wiener Filter</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In the previous discussion, we derived and illustrated the discrete-time Wiener filter for the FIR and non-causal IIR cases. In this section we derive the continuous-time counterpart of the result for the non-causal IIR Wiener filter. The DT derivation involved taking derivatives with respect to a (countable) set of parameters h[m], but in the CT case the impulse response that we seek to compute is a CT function h(t), so the DT derivation cannot be directly copied. However, you will see that the results take the same form as in the DT case; furthermore, the derivation below has a natural DT counterpart, which provides an alternate route to the results in the preceding section.</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-28.png" width="602" height="109" alt="" />
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Fig: CT LTI filter for linear MMSE estimation</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Let x(t) be a (zero-mean) WSS random process that we have measurements of.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We want to determine the impulse response or frequency response of the above LTI system such that the filter output y</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">(t) is the LMMSE estimate of some (zero-mean)</span><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">“target” process y(t) that is jointly WSS with x(t). We can again write</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-29.png" width="212" height="79" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxix)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Assuming the filter is stable (or at least has a well-defined frequency response), the process y</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sup>^</sup></span><span style="font-family:'Times New Roman'">(t) is jointly WSS with x(t). Furthermore,</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-30.png" width="425" height="38" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxx)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The quantity we want to minimize can again be written as</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-31.png" width="237" height="37" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">where the error autocorrelation function R</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>ee</sub></span><span style="font-family:'Times New Roman'">(τ ) is — using the definition in equation (xxix)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">— evidently given by</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-32.png" width="470" height="39" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Thus</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-33.png" width="523" height="137" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxiii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Our task is now to choose H(jω) to minimize the integral in equation (xxxiii). We can do this by minimizing the integrand for each ω. The first term in the integrand does not involve or depend on H, so in effect we need to minimize</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-34.png" width="413" height="33" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxiv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">is minimization would be straight forward. Even with a complex H and Syx, however, the minimization is not hard. The key to the minimization is an elementary technique referred to as completing the square. For this, we write the quantity in equation (xxxiv) in terms of the squared magnitude of a term that is linear in H. This leads to the following rewriting of equation (xxxiv):</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-35.png" width="522" height="59" alt="" style="margin-right:9pt; margin-left:9pt; float:left; position:relative" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In writing √S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">, we have made use of the fact that S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) is real and nonnegative. We have also felt free to divide by √S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) because for any ω where this quantity is 0 it can be shown that S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">(jω) = 0 also. The optimal choice of H(jω) is therefore arbitrary at such ω, as evident from equation (xxxiv). We thus only need to compute the optimal H at frequencies where √S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) &gt; 0.</span><br /><span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Notice that the second term in parentheses in equation (xxxv) is the complex conjugate of the first term, so the product of these two terms in parentheses is real and nonnegative. Also, the last term does not involve H at all. To cause the terms in parentheses to vanish and their product to thereby become 0, which is the best we can do, we evidently must choose as follows (assuming there are no additional constraints such as causality on the estimator):</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-36.png" width="201" height="56" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxvi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">This expression has the same form as in the DT case. The formula for H(jω) causes it to inherit the symmetry properties of S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>yx</sub></span><span style="font-family:'Times New Roman'">(jω), so H(jω) has a real part that is even in ω, and an imaginary part that is odd in ω. Its inverse transform is thus a real impulse response h(t), and the expression in equation (xxxvi) is the frequency response of the optimum (Wiener) filter.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-37.png" width="460" height="190" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxvii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">where the function ρ(jω) is defined by</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-38.png" width="282" height="48" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxviii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">and evidently plays the role of a (complex) frequency-by-frequency correlation co-efficient, analogous to that played by the correlation coefficient of random variables Y and X</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">Causal Wiener Filtering</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">In the preceding discussion we developed the Wiener filter with no restrictions on the filter frequency response H(jω). This allowed us to minimize a frequency domain integral by choosing H(jω) at each ω to minimize the integrand. However, if we constrain the filter to be causal, then the frequency response cannot be chosen arbitrarily at each frequency, so the previous approach needs to be modified. It can be shown that for a causal system the real part of H(jω) can be determined from the imaginary part, and vice versa, using what is known as a Hilbert transform. This shows that H(jω) is constrained in the causal case. (We shall not need to deal explicitly with the particular constraint relating the real and imaginary parts of H(jω), so we will not pursue the Hilbert transform connection here.) The development of the Wiener filter in the causal case is therefore subtler than the unrestricted case, but you know enough now to be able to follow the argument.</span>
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-39.png" width="602" height="102" alt="" />
			</p>
			<p style="text-align:center; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Fig: Representation of LMMSE estimation using an LTI system.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The input x(t) is a (zero-mean) WSS random process that we have measurements of, and we want to determine the impulse response or frequency response of the above LTI system such that the filter output yb(t) is the LMMSE estimate of some (zero-mean) “target” process y(t) that is jointly WSS with x(t):</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-40.png" width="204" height="81" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxix)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">We shall now require, however, that the filter be causal. This is essential in, for example, the problem of prediction, where y(t) = x(t + t0) with t0 &gt; 0. We have already seen that the quantity we want to minimize can be written as</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-41.png" width="602" height="182" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxx)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The last equality was the result of “completing the square” on the integrand in the preceding integral. In the case where H is unrestricted, we can set the first integral of the last equation to 0 by choosing</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-42.png" width="191" height="47" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxxi)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">at each frequency. The second integral of the last equation is unaffected by our choice of H, and determines the MMSE.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">If the Wiener filter is required to be causal, then we have to deal with the integral</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-43.png" width="324" height="50" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxxii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">as a whole when we minimize it, because causality imposes constraints on H(jω) that prevent it being chosen freely at each ω. (Because of the Hilbert transform relationship mentioned earlier, we could for instance choose the real part of H(jω) freely, but then the imaginary part would be totally determined.) We therefore have to proceed more carefully.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Note first that the expression we obtained for the integrand in equation (xxxxii) by completing the square is actually not quite as general as we might have made it. Since we may need to use all the flexibility available to us when we tackle the constrained problem, we should explore how generally we can complete the square. Specifically, instead of using the real square root √Sxx of the PSD Sxx, we could choose a complex square root Mxx, defined by the requirement that</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-44.png" width="448" height="35" alt="" /><span style="font-family:'Times New Roman'">&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxxiii)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">and correspondingly rewrite the criterion in equation (xxxxii) as</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-45.png" width="300" height="51" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxxiv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">which is easily verified to be the same criterion, although written differently. The quantity M</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) is termed a spectral factor of S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) or a modeling filter for the process x. The reason for the latter name is that passing (zero-mean) unit-variance white noise through a filter with frequency response M</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) will produce a process with the PSD S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω), so we can model the process x as being the result of such a filtering operation. Note that the real square root √S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) we used earlier is a special case of a spectral factor, but others exist. In fact, multiplying √S</span><span style="line-height:108%; font-family:'Times New Roman'; font-size:9.33pt; "><sub>xx</sub></span><span style="font-family:'Times New Roman'">(jω) by an all-pass frequency response A(jω) will yield a modeling filter:</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<img src="1736155213_wiener-filter/1736155213_wiener-filter-46.png" width="441" height="39" alt="" /><span style="font-family:'Times New Roman'">&#xa0;&#xa0; </span><span style="font-family:'Times New Roman'">… (xxxxv)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">Conversely, it is easy to show that the frequency response of any modeling filter can be written as the product of an all-pass frequency response and √Sxx(jω). It turns out that under fairly mild conditions (which we shall not go into here) a PSD is guaranteed to have a spectral factor that is the frequency response of a stable and causal system, and whose inverse is also the frequency response of a stable and causal system. (To simplify how we talk about such factors, we shall adopt an abuse of terminology that is common when talking about Fourier transforms, referring to the factor itself — rather than the system whose frequency response is this factor — as being stable and causal, with a stable and causal inverse.)</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:18pt">
				<strong><span style="font-family:'Times New Roman'; ">Applications</span></strong><strong><span style="width:41.98pt; font-family:'Times New Roman'; display:inline-block">&#xa0;</span></strong>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">The Wiener filter has a variety of applications in signal processing, image processing, control systems, and digital communications. These applications generally fall into one of four main categories:</span>
			</p>
			<ul style="margin:0pt; padding-left:0pt">
				<li class="ListParagraph" style="margin-left:29.44pt; margin-bottom:0pt; text-align:justify; line-height:108%; padding-left:6.56pt; font-family:serif; font-size:14pt">
					<span style="font-family:'Times New Roman'">System identification</span>
				</li>
				<li class="ListParagraph" style="margin-left:29.44pt; margin-bottom:0pt; text-align:justify; line-height:108%; padding-left:6.56pt; font-family:serif; font-size:14pt">
					<span style="font-family:'Times New Roman'">Deconvolution</span>
				</li>
				<li class="ListParagraph" style="margin-left:29.44pt; margin-bottom:0pt; text-align:justify; line-height:108%; padding-left:6.56pt; font-family:serif; font-size:14pt">
					<span style="font-family:'Times New Roman'">Noise reduction</span>
				</li>
				<li class="ListParagraph" style="margin-left:29.44pt; text-align:justify; line-height:108%; padding-left:6.56pt; font-family:serif; font-size:14pt">
					<span style="font-family:'Times New Roman'">Signal detection</span>
				</li>
			</ul>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">For example, the Wiener filter can be used in image processing to remove noise from a picture. It is commonly used to denoise audio signals, especially speech, as a pre-processor before speech recognition.</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
			<p style="text-align:justify; line-height:108%; font-size:14pt">
				<span style="font-family:'Times New Roman'">&#xa0;</span>
			</p>
	<p style="bottom: 10px; right: 10px; position: absolute;"><a href="https://wordtohtml.net" target="_blank" style="font-size:11px; color: #d0d0d0">Converted to HTML with WordToHTML.net</a></p>
</body>
</html>