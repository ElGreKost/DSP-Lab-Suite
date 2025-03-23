# DSP Lab Suite

DSP Lab Suite is a collection of hands-on lab projects and experiments in digital signal processing using Python. This repository contains the submission for the first lab assignment of the Digital Signal Processing course (2022–2023) at N.T.U.A. It covers fundamental concepts through experiments on spectral analysis, telephone touch-tone systems, and short-time signal characteristics.

## Overview

The lab assignment is divided into three main parts:

1. **Part 1 – Spectral Analysis and Sinusoid Detection**  
   - **Objective:** Analyze the spectral resolution of signals composed of two sinusoids.  
   - **Experiments include:**  
     - Computing the Discrete Fourier Transform (DFT) of a windowed sum of two sinusoids.  
     - Examining the effects of different DFT lengths (256, 512, 1024 points), zero-padding, and windowing (rectangular vs. Hamming).  
     - Determining the minimum frequency separation (Δω) needed to resolve two peaks.

2. **Part 2 – Telephone Touch-Tone System**  
   - **Objective:** Simulate the generation and decoding of telephone touch-tones.  
   - **Experiments include:**  
     - Generating 10 different telephone tones, each 1000 samples long, based on predefined frequency pairs (columns and rows).  
     - Computing and plotting the DFT (1024 points) of selected tones.  
     - Creating a “tone sequence” WAV file by mapping the sum of student IDs (or a single student ID) to a sequence of tones with 100 zero-sample gaps between digits.  
     - Implementing a `ttdecode` function that decodes a tone sequence into its corresponding digit vector.  
     - Testing the decoder using additional signals (e.g., easy, medium, hard) provided in complementary materials.

3. **Part 3 – Short-Time Analysis of Voice and Music Signals**  
   - **Objective:** Extract short-time features from speech and music signals.  
   - **Experiments include:**  
     - Plotting a voice signal (from “speech_utterance.wav”) in the time domain.  
     - Computing short-time energy and zero-crossing rate using 20–50 ms windows.  
     - Calculating the spectral centroid and spectral flux via the Short-Time Fourier Transform (STFT) (using 2048-point FFT) and examining the effect of varying window lengths.  
     - Repeating the analysis for a music signal (converted from stereo to mono).

## Repository Structure

```
DSP-Lab-Suite/
├── button_frequencies_matrix.jpg  
├── code.ipynb  
├── Instructions.pdf  
├── Lab1_Data  
│   ├── easy_sig.npy  
│   ├── hard_sig.npy  
│   ├── medium_sig.npy  
│   ├── music_changed_changed.wav  
│   ├── music_mono.wav  
│   └── speech_utterance_changed.wav  
├── speech_utterance.wav  
└── tone_sequence.wav
```

## Getting Started

### Prerequisites

- **Python 3.x**  
- [Jupyter Notebook](https://jupyter.org/)  
- Python libraries: `numpy`, `scipy`, `matplotlib`, `IPython`, `soundfile` (or `scipy.io.wavfile`), etc.  
- (Optional) **FFmpeg** for audio processing ([FFmpeg Installation Guide](https://ffmpeg.org/download.html))

### Running the Lab Code

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ElGreKost/DSP-Lab-Suite.git
   ```
2. **Navigate to the lab directory:**
   ```bash
   cd DSP-Lab-Suite
   ```
3. **Launch the Jupyter Notebook:**
   ```bash
   jupyter notebook Lab1_Code.ipynb
   ```
4. **Follow the instructions in the notebook:**  
   - **Part 1:** Modify sinusoid frequencies, compute DFTs, and plot amplitude spectra to investigate resolution limits.  
   - **Part 2:** Generate telephone touch-tone signals, compute their DFTs, create a tone sequence WAV file, and test the `ttdecode` function.  
   - **Part 3:** Compute short-time energy, zero-crossing rate, STFT, spectral centroid, and spectral flux for speech and music signals.

## Submission Details

- **Report:** The detailed lab report (Lab1_Instructions.pdf) includes methodology, experimental results, plots, and responses to the lab questions.  
- **Tone Sequence:** The generated file `Lab1_ToneSequence.wav` is included as part of the deliverables.  
- **Code:** The `Lab1_Code.ipynb` notebook contains all Python code used for the experiments.

## Contributing

Contributions, suggestions, and improvements are welcome! Feel free to fork the repository and submit pull requests. For major changes or new experiments, please open an issue first to discuss your ideas.

## License

Distributed under the MIT License. See the `LICENSE` file for more details.
