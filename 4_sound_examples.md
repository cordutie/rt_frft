<p>
This section presents a set of sound examples illustrating the methods introduced in Section 5. To highlight both the real-time capabilities of our implementation and the geometric interpretability of the FRFT, all examples except the final one were recorded as videos using our real-time Max implementation and are accompanied by spectrograms.
</p>

<div style="margin-top: 20px;"></div>

<!-- ======================= 6.1 ======================= -->
<details open>
<summary>
<span style="font-weight: normal; font-size: 1.5em; color: black">
6.1. α–Synthesis and Processing Examples 🎧
</span>
</summary>

<div style="margin-top: 20px;"></div>

<p>
The following examples illustrate the α-synthesis and processing techniques.
</p>

<!-- 6.1.1 -->
<h3>6.1.1. Vanilla Synthesis Examples</h3>
<p>
A sinusoid at 440~Hz was synthesized using all combinations of the following parameters: window sizes of 2048 and 65536 samples; hop sizes equal to the full window, half, and one quarter; and α in {0,0.01,0.1,0.4}. This configuration provides a broad parameter space to examine the effect of the RFRFT on pure tones. The experiment was repeated using a square wave at the same frequency.
</p>

<p>
Large windows clearly reveal the chirp-like transformations induced by the double rotation property. With smaller windows, the chirps become sufficiently steep to be perceived as novel sound textures, occasionally producing emergent pitch sensations. Varying the hop size enables further control over the resulting textures.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%;">
    <video controls style="width: 100%; height: auto;">
      <source src="assets/videos/6.1.1 Vanilla Synthesis examples - Sine Input.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%;">
    <video controls style="width: 100%; height: auto;">
      <source src="assets/videos/6.1.1 Vanilla Synthesis examples - Square Input.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<!-- Previous Paper:
<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/B0pOn1DQwiY"
      title="Alpha Synthesis with Parameter Modulation"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div> -->

<!-- 6.1.2 -->
<h3>6.1.2. Synthesis + Parameter manipulation example</h3>
<p>
Here, the order of the FRFT is dynamically modulated while overlap-and-add parameters remain fixed. Sinusoids and square waves are again used as inputs, with α controlled in real time via an LFO. Even with simple source signals, this approach yields a wide range of continuously evolving textures, demonstrating sophisticated control possibilities.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/bGcGklXBB9Y?si=Y29V4mLBUvlzm6Ja"
      title="Alpha Synthesis with Parameter Modulation"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>



<!-- 6.1.3 -->
<h3>6.1.3. Minimal Processing Examples</h3>
<p>
Two audio excerpts, a percussed clarinet and a staccato string ensemble texture, were α-processed using the same parameter combinations as in Example 6.3.1.
</p>

<p>
Partials in the input signals are transformed into frequency-modulated tones, while noisier components remain noise-like but acquire tonal coloration due to excited chirps in the α-domain. Window and hop size again play a significant role in shaping the resulting textures.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/iF-Jg9fFQ-A"
      title="Minimal Alpha Processing"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/eE98i4gutgQ?si=xYyIErbqNeGwwYDL"
      title="Minimal Alpha Processing"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%;">
    <video controls style="width: 100%; height: auto;">
      <source src="assets/videos/6.1.3 Minimal processing examples - untitled02.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<!-- 6.1.4 -->
<h3>6.1.4. Processing + Parameter Manipulation</h3>
<p>
A collection of percussive, synthetic pitched, and acoustic pitched sounds was processed using the RFRFT with order modulated in real time by an LFO. Percussive sounds retain sharp transients for small windows while resonant components are transformed into audible chirps. Complex pitched sounds become collections of non-harmonically related chirps whose structure evolves over time, producing metallic and time-varying timbres.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/VmrND7O0xfU"
      title="Alpha Processing with Modulation"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/QJM4CAQ_jWw?si=YZGKGstFsPxyTSoB"
      title="Alpha Processing with Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

</details>


<!-- ======================= 6.2 ======================= -->
<div style="margin-top: 20px;"></div>
<details open>
<summary>
<span style="font-weight: normal; font-size: 1.5em; color: black">
6.2. α–Filters and Convolution Examples 🎛️
</span>
</summary>

<div style="margin-top: 20px;"></div>

<p>
These examples illustrate the α-filtering and convolution methods
</p>

<h3>6.2.1. Vanilla Filters</h3>
<p>
White noise was α-filtered using various band-pass filters to explore perceptual characteristics of different regions in the α-domain. Parameters included window sizes of 32768 and 2048 samples; α in {0,0.1,0.5}; hop sizes equal to a fourth, a half, and a full window; and manually controlled filter kernels. The experiment was repeated using a 440~Hz sinusoid.
</p>

<p>
The resulting bands correspond not to fixed frequencies but to chirps whose modulation depends on α and window size. For the sinusoid, prominent energy bands appear across the α-domain for all orders, with markedly different sonic characteristics as α varies.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/Q5bxa2bTDeE"
      title="Vanilla Alpha Filters"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/39ZL2P9e8dE?si=5_HCxzyER7VH0n74"
      title="Vanilla Alpha Filters 3"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/GsHaqQHi5YI?si=-8tyjDr6UW5EJF-n"
      title="Vanilla Alpha Filters 2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<h3>6.2.2. Filters + Parameter Manipulation</h3>
<p>
A string ensemble and a sung voice were processed using α-filters with time-varying α. Small windows produce heavily distorted yet input-coherent signals, reminiscent of bit crushing or fuzz. The spectral color of this distortion is controllable via α-domain band selection and can introduce metallic qualities. With larger windows, α low-pass filtering yields rhythmic amplitude-modulation effects while preserving intelligibility.</p>


<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/qRO3LAE-oWQ?si=RsWiQIoaSxY0VaSR"
      title="Filters with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/YTlvPGFpkXk?si=Xv9Nko6BthjAqawZ"
      title="Filters with Parameter Modulation 2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/nbXRuLykpE8?si=MIiAL_hHAtKa2WF_"
      title="Filters with Parameter Modulation 3"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/FnxI465W378?si=L31LxMsTgPUqsCPB"
      title="Filters with Parameter Modulation 4"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<h3>6.2.3. Vanilla Convolutions</h3>
<p>
Several sounds including a sinusoid, a drum pattern, and a sung voice, were α-convolved with square waves using fixed parameters. Window and hop sizes matched those in Example 6.3.1, with α in {0,0.01,0.1}.
</p>

<p>
Large windows smooth transients, reducing rhythmic clarity in the drum pattern. Smaller windows preserve transients and introduce a bit-crushed quality. The sinusoid yields synthetic pitched sounds, while the sung voice produces textures similar to those obtained through α-filtering.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/Tlfh544izOs?si=ldVDGAY3OZG_u3bC"
      title="Vanilla Alpha convolutions 3"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/vBwMrA1nbMc?si=z2wGv0NmxdAUlVyZ"
      title="Vanilla Alpha convolutions 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/-nStXowsfT8?si=Ax6Joj68dhie61VN"
      title="Vanilla Alpha convolutions 2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<h3>6.2.4. Convolution + Parameter Manipulation</h3>
<p>
Pairs of sounds, including a sinusoid with a square wave and a sung voice with itself, were α-convolved while modulating α in real time. The sinusoid–square wave pair produces frequency-modulated pitched noise, while the self-convolved voice generates structured chirp systems that retain many perceptual qualities of the original signal for large windows and small α.</p>


<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/kGieKa5G9xs?si=O0EQL2KFPbTACICQ"
      title="Convolutions with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/hAefS-V7fjk?si=DtV6UEis-h3g4LJ3"
      title="Convolutions with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/YTKGFlbmir4?si=dqsOpuPL9DK3IN0Z"
      title="Convolutions with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

</details>

<!-- ======================= 6.3 ======================= -->
<div style="margin-top: 20px;"></div>
<details open>
<summary>
<span style="font-weight: normal; font-size: 1.5em; color: black">
6.3. α–Ring Modulation Examples 🔄
</span>
</summary>

<div style="margin-top: 20px;"></div>

<p>
These examples demonstrate α-ring modulation.
</p>

<h3>6.3.1. Vanilla Ring Modulation</h3>
<p>
A triangular wave and an acoustic guitar excerpt were used as carriers, with a triangular wave as modulator. Carrier parameters matched those of Examples 6.3.1. The modulator order α_m was defined relative to the carrier order α_c as α_m in {α_c,2α_c,1-α_c,-α_c}.
</p>

<p>
Using α_m=α_c or 2α_c generally produces similar outcomes. For small α, results resemble standard ring modulation. Larger α values yield stronger frequency modulation for α_m=1-α_c, while α_m=-α_c produces interference patterns perceived as rhythmic structures, consistent with the multiplication of oppositely directed chirps.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/B0pOn1DQwiY"
      title="Alpha Ring Modulation"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/SUdOmrFiFps?si=JAzN01Y21OEAtMCw"
      title="Alpha Ring Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/1QliTatOTAw?si=VwcrEkavl1u5-0fw"
      title="Alpha Ring Modulation 2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<h3>6.3.2. Ring Modulation + Parameter Manipulation</h3>
<p>
Using the same sound material as in the previous example, α was modulated in real time via an LFO. Time-varying α enables continuous navigation between the behaviors observed in the static case, making the perceptual impact of α modulation particularly salient.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/jRxrkIlauac?si=ciIKpusa_0a3cDmx"
      title="Alpha Ring Modulation with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/c2ZWm98VLiU?si=bquHC3JB5_nfcSRF"
      title="Alpha Ring Modulation with Parameter Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


</details>


<!-- ======================= 6.4 ======================= -->
<div style="margin-top: 20px;"></div>
<details open>
<summary>
<span style="font-weight: normal; font-size: 1.5em; color: black">
6.4. Other Examples 🌌
</span>
</summary>

<div style="margin-top: 20px;"></div>

<h3>6.4.1. Feedback Structures</h3>
<p>
A sinusoid is processed within a feedback loop in which the output of the α-processing stage is reinjected into its input. This configuration produces chaotic, evolving, and non-repeating sound textures.
</p>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/R5FmsEVHGGM?si=Ll8jQASiTCJxKR0R"
      title="Feedback"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<h3>6.4.1. Rhythmic Patterns </h3>
<p>
Sub-audible frequencies are used in α-synthesis with α close to 1. These components are transformed into broadband chirps. With small windows, this results in complex rhythmic patterns composed of short, irregular resonances.
</p>

<!-- Via Synthesis: -->

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/H7xIomGsXwY?si=D0fQz55JRJ-aWxNt"
      title="rhythmic"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

<!-- Via filter manipulation (voice input - most prominent around 1.30): -->

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/sXDVyswQuEc?si=_UGaTdGzWtMvd3Nm"
      title="rhythmic2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<!-- <h3>6.4.2. Soundscape Generation using Giant RFRFT</h3>
<p>
This example explores a technique inspired by zero-phase sound processing,
replacing the Fourier transform with FRFTs of different orders.
</p>

</details> -->