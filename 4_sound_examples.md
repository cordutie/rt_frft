<p>
Several videos and sound examples illustrating the methods presented in this article are included below.
Most examples were recorded as videos using our real-time implementation in Max/MSP and are accompanied
by spectrograms for detailed time–frequency analysis.
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
The following examples demonstrate the α–synthesis and processing techniques described in
Section 5.1. These examples highlight both the real-time capabilities of the implementation
and the geometric interpretability of the FRFT.
</p>

<!-- 6.1.1 -->
<h3>6.1.1. Vanilla Synthesis Examples</h3>
<p>
These examples showcase basic α–synthesis applied to standard harmonic waveforms
(sine, sawtooth, square) with fixed α values, illustrating fundamental chirp-like
transformations.
</p>

<p>
For small window sizes, the resulting chirps are so steep that they are perceived as
percussive elements and manifest as a new pitch. For larger windows, the chirps lose
this quality and can be perceived as frequency-modulated sinusoids. Additional examples
demonstrate the influence of hop size on artifact control. Further examples employ only
half of the spectrum, as shown in Figure 8.
</p>

Sinusoidal Input:

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%;">
    <video controls style="width: 100%; height: auto;">
      <source src="assets/videos/6.1.1 Vanilla Synthesis examples - Sine Input.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

Square Input:

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%;">
    <video controls style="width: 100%; height: auto;">
      <source src="assets/videos/6.1.1 Vanilla Synthesis examples - Square Input.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

Previous Paper:
<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/B0pOn1DQwiY"
      title="Alpha Synthesis with Parameter Modulation"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<!-- 6.1.2 -->
<h3>6.1.1. Synthesis + Parameter manipulation example</h3>
<p>
This example features dynamic modulation of the order of the FRFT with fixed overlap-and-add parameters. 
The dynamic modulation is performed in real time, where control over the spectral evolution and the perceived 
slope of the generated chirps is achieved using different LFOs. The results reveal a large number of non-trivial 
ways of exerting control in the synthesis process, which in turn generate a wide variety of sound textures, 
even when the synthesis is driven by simple waveforms.
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
A first set of examples contains short excerpts of wind instruments, sung voice,
and electronic keyboards processed with conservative and static α values. These
examples highlight subtle frequency-modulated complexes of tones caused by the
double-rotation property.
</p>




<p>
A second set uses spectrally complex material and less conservative α values,
resulting in a wide variety of sound textures that disrupt harmonic organization
or render percussive sounds noisier while preserving amplitude envelopes.
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
Percussive, synthetic pitched, and acoustic pitched sounds are processed using the
RFRFT with the order modulated in real time by an LFO.
</p>

<p>
Percussive sounds retain their transients while resonances become perceptible chirps.
Pitched sounds are transformed into inharmonic sums of chirps that evolve dynamically,
resulting in metallic, time-varying timbres.
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

</details>

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/QJM4CAQ_jWw?si=YZGKGstFsPxyTSoB"
      title="Alpha Processing with Modulation 1"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


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
These examples pertain to the α–filtering and convolution techniques discussed in
Section 5.2.
</p>

<h3>6.2.1. Vanilla Filters</h3>
<p>
Examples include extracting complex sounds from α–filtered white noise, illustrating
that α–domain bands correspond to chirps rather than pure frequencies.
</p>

<p>
Further experiments use sinusoidal and square-wave inputs to expose how signals
decompose across different α–domains.
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
TO DO
</p>


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
TO DO
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
TO DO
</p>


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
Examples of α–ring modulation are presented here. In all cases, versions using
only half of the spectrum are also included.
</p>

<h3>6.3.1. Vanilla Ring Modulation</h3>
<p>
The basic α–RM effect is demonstrated by multiplying the FRFTs of two sinusoids,
yielding a characteristic four-component chirp structure.
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
More complex interactions are achieved by modulating the α parameter of both carrier
and modulator in real time, producing dynamically shifting inharmonic spectra.
</p>

<p>
Note: Using sinusoids with opposite angles results in a cancellation of the rotation.
</p>

</details>


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
Different signals are used within feedback structures that route the output of
α–processing back into its own input, producing chaotic systems.
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

Rhythmic Patterns at alpha near 1 (RFRFT close to FT):

Via Synthesis:

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/H7xIomGsXwY?si=D0fQz55JRJ-aWxNt"
      title="rhythmic"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>

Via filter manipulation (voice input - most prominent around 1.30):

<div style="margin-top: 20px; display: flex; justify-content: center;">
  <div style="position: relative; width: 66%; padding-top: 37.5%;">
    <iframe src="https://www.youtube.com/embed/sXDVyswQuEc?si=_UGaTdGzWtMvd3Nm"
      title="rhythmic2"
      frameborder="0" allowfullscreen
      style="position:absolute; top:0; left:0; width:100%; height:100%;">
    </iframe>
  </div>
</div>


<h3>6.4.2. Soundscape Generation using Giant RFRFT</h3>
<p>
This example explores a technique inspired by zero-phase sound processing,
replacing the Fourier transform with FRFTs of different orders.
</p>

</details>