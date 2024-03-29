<div align="center">
<h1> <b> Mouse-Synthesizer</b></h1>
<p>The most advanced mouse movement synthesizer based on the human hand <b>biometric</b> theory</p>
<img src="https://avatars.githubusercontent.com/u/121403675?s=400&u=4ce7a2f06e85191ad4e375ea7128b5b5717baf8a&v=4)">
</div>

# Description

A deep dive into the abstruse ocean of human hand biometrics. 
The project sets to unravel the buried secrets concealed behind the NeuroPhysiological basis of the human mouse movements. 

<b>MIMIC aims to synthesize human-like mouse movements</b>, in their minute detail.
Negligible was not a word we ever considered throughout our journey, we aspire to achieve perfection and consistency at any generation.

# Uniqueness

<li><a href="#human-behaviour">Human-Behaviour</a></li>
<li><a href="#flexibility">Flexibility</a></li>
<li><a href="#consistency">Consistency</a></li>

# Human-Behaviour

The project is built on human biometric theory, thus almost impossible to be recognized by any form of antibots nor human.
In the image below, one is a real human generated movement(blue), the other is a synthesized trajectory from MIMIC.
More images are avaible <a href="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/tree/main/images">here</a>.

<img src="https://raw.githubusercontent.com/MIMIC-LOGICS/Mouse-Synthesizer/main/images/sample_1.png">

## Flexibility

Highly customizable in every aspect.

- Customizable number of <b>stops</b> at each generation. Each stop increases the level of complexity of the overall trajectory. Stops are point of more noticeable change in velocity, and, for istance, can be overshooting positions or mouse clicks.
  - Customizable <b>starting</b> and <b>ending position</b> of each stop</li>
  - Customizable <b>time</b> occurence of each stop  </li>
  - Customizable bounding box between stops (<i>soon</i>)
- Customizable <b>Noise</b><br>
  Define the SNR of the signal. Look at examples <a href="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/tree/main/images/SNR">here</a>.

- Customizable <b>Sampling Frequency</b> of the movement<br>
  Choose the frequency you want MIMIC to sample at, all range admitted. It is also possible to randomize the frequency generation making it <b>non         uniform</b>. In the example below, a non uniform frequency of 200Hz is used.
  <img src="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/blob/main/images/frequency/sample_200HZ.png">

- Customizable <b>Screen dimension</b><br>
  Define a custom screen dimension, so that the natural evolution of the mouse trajectory will be bounded to the choosen box dimension.
  In other terms, the mouse trajectory will not end outside the screen. In the example below the screen used was 1280x1280.
  <img src="https://raw.githubusercontent.com/MIMIC-LOGICS/Mouse-Synthesizer/main/images/self-correcting/self-correcting4.png">

 

# Consistency

MIMIC is able to generate valid synthesized trajectory consistently, without being flagged by any type of algorithm.
Particular attention was addressed to the stabilization of the system, so that the probability of generating unstable/inaccurate results is made very low. 

# Comparison

Here's a short comparison with some common mouse synthesizers on the market.<br>
Multiple amplitude spectrum from the X,Y positions of mouse data, sampled at a uniform frequency of 60Hz, were compared. The comparison is not accurate, since it assumes an uniform time, and each movement differs in terms of sampling size from the other (it was not normalized with PSD). However it is sufficient to draw based conclusion about the greatness of MIMIC compared to the other solutions.

<div align="center">
<i><b> REAL mouse spectrum</b> </i>
<img src="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/blob/main/images/spectrum/REAL/REAL-6.png">

<br><br>
<i><b> Bot B  </b></i>
<img src="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/blob/main/images/spectrum/botB/botb_sample.png">
<br><br><a href="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/tree/main/images/spectrum/botB">Bot B </a> spectrum does not resemble real movements spectrum, with the content spectrum sharply fluctuating at different near frequencies. Although this solution is popular it underperforms, and could be flagged in a frequency-domain analysis.
<br><br>

<i><b> Bot A</b> </i>
<img src="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/blob/main/images/spectrum/botA/MACT-1.png">

<br><a href="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/tree/main/images/spectrum/botA">Bot A</a> performs better than bot B, however it generates a spectrum content spread over the whole signal bandwidth, resembling a white noise spectrum. <br> We may speculate that it was generated with some sort of Gaussian Algorithm and high-frequency noise, and has only some characteristic that resembles a real signal. <br>This spectrum may actually pass a spectrum analysis check, however, the fact that the movements synthesized are always the same could hurt an API generator after a few generations.

<br><br>

<i><b> Mimic </b> </i>
<img src="https://github.com/MIMIC-LOGICS/Mouse-Synthesizer/blob/main/images/spectrum/MIMIC/GENERATED-1.png">
<br><b> Mimic </b> outperforms every synthetizer, and propose an analogous spectrum to the real signal spectrum, making it indistinguishable in a frequency analysis. The spectrum is different and reliable at all generations.

<br>
</div>

# Acknowledgements

Many thanks to <b>M-NK-Y</b> who has always been of great support and inspired me to make of this project what it is now.
