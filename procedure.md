<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body>
  <ul>
    <li>
      <strong>Input Parameters:</strong>
      <ul>
        <li><strong>Input Signal(s):</strong> Specify the type of signal (sine, cosine, amplitude modulated (AM) signal, or double sideband suppressed carrier signal) from the dropdown options, and enter the frequency values of the signal(s).</li>
        <li><strong>Sampling Frequency (in Hz):</strong> Enter the sampling frequency in the input field.</li>
        <li><strong>Filter Order:</strong> Enter the order of the Wiener filter.</li>
        <li><strong>SNR (in dB):</strong> Enter the desired Signal-to-Noise Ratio (SNR) in decibels (dB).</li>
      </ul>
    </li>
        <br/>
    <h3><strong>Steps:</strong></h3>
    <li>
      <strong>1. Generate Input Signal:</strong> 
      Click the <em>“Generate Message”</em> button to generate the input signal.
    </li>
    <li>
      <strong>2. Generate Noisy Signal:</strong> 
      Click the <em>“Generate Noisy Signal”</em> button to add Additive White Gaussian Noise (AWGN) to the input signal and generate the noisy signal.
    </li>
    <li>
      <strong>3. Display Power Spectral Density (PSD) of the Noisy Signal:</strong> 
      Click the <em>“Show PSD for Noisy Signal”</em> button to visualize the PSD of the noisy signal.
    </li>
    <li>
      <strong>4. Show Wiener Filter Coefficients:</strong> 
      Click the <em>“Show Filter Coefficients”</em> button to visualize the Wiener filter coefficients, which minimize the error between the estimated signal and the original input message signal.
    </li>
    <li>
      <strong>5. Generate the Estimated Signal:</strong> 
      Click the <em>“Generate Estimated Signal”</em> button to visualize the estimated signal produced as the Wiener filter output.
    </li>
    <li>
      <strong>6. Generate the Residual Signal:</strong> 
      Click the <em>“Generate Residual Signal”</em> button to display the difference between the original input message signal and the filtered signal.
    </li>
  </ul>
</body>
</html>
