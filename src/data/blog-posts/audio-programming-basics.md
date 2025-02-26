---
title: 🎛️ APB ep.1 - The Core Elements of Sound
publishDate: 26.02.2025
description: Essential guide & cheatsheet for core elements of sound.
---

**Welcome to the Audio Programming Basics Series!**


This series of articles is meant to be a starting point into the world of audio programming, aimed for beginners or to brush up on the fundamentals. This series will guide you step-by-step. <br/>
We'll start on the most essential concept: **the core elements of sound**.

<hr>

All sounds is just *vibrations in the air* that our ears perceive. In digital audio, we break sound down into key elements.

### 1. Frequency (Pitch) - The *Note* of Sound
- Measured in *Hertz (Hz)*
- **Low frequency** = *Deep/Bass sounds* (e.g. 60 Hz = subwoofer rumble)
- **High frequency** = *Sharp/Treble sounds* (e.g. 5000 Hz = whistle)
- The human hearing range is **20 Hz - 20,000 Hz**

🔹 **Example**: A standard musical **A4** note is **440 Hz**.

### 2. Amplitude (Loudness) - The *Volume* of Sound
- Measured in *decibels (dB)*
- **Higher amplitude** = *Louder sound*
- **Lower amplitude** = *Softer sound* 
- In digital audio, amplitude is usually in a range of **-1** to **1** (normalized).

🔹 **Example**: Whispering is about **30 dB**, while a jet engine is **120 dB**.

### 3. Waveforms - The *Shape* of Sound
- **Sine Wave (Pure Tone)** - Soft and smooth (e.g., tuning fork)
- **Square Wave** - Harsh, buzzy sound (used in retro game music)
- **Triangle Wave** - Softer than a square wave, more flute-like
- **Sawtooth Wave** - Bright and sharp, used in synths

🌀 **Example**: Let’s generate different waveforms in Python:
```python
import numpy as np
import sounddevice as sd

def generate_waveform(wave_type="sine", freq=440, duration=1.0, sample_rate=44100):
    t = np.linspace(0, duration, int(sample_rate * duration), False)
    
    if wave_type == "sine":
        wave = np.sin(2 * np.pi * freq * t)
    elif wave_type == "square":
        wave = np.sign(np.sin(2 * np.pi * freq * t))
    elif wave_type == "triangle":
        wave = 2 * np.abs(2 * (t * freq - np.floor(t * freq + 0.5))) - 1
    elif wave_type == "sawtooth":
        wave = 2 * (t * freq - np.floor(0.5 + t * freq))
    else:
        raise ValueError("Unknown waveform type")
    
    return 0.3 * wave  # Reduce volume

# Play a sawtooth wave
wave = generate_waveform("sawtooth", 440)
sd.play(wave, samplerate=44100)
sd.wait()

```
Try changing "sawtooth" to "sine", "square", or "triangle" and hear the difference! 🎧

## 4. Sample Rate – *How Often* We Capture Sound
- Measured in samples per second (Hz)
- Common sample rates:
    - 🎤 44,100 Hz (CD Quality)
    - 🎼 48,000 Hz (Studio Quality)
    - 🎬 96,000 Hz (High-Fidelity Audio Production)

🔹 **Analogy**: A higher sample rate is like a high-frame-rate video—smoother, more detailed sound.

## 5. Bit Depth – The **Detail** in Sound
- Controls resolution (how accurately we store amplitude levels)
- Common bit depths:
    - 🎧 16-bit (CD Quality)
    - 🎵 24-bit (Studio Quality, more dynamic range)
    - 🔊 32-bit (Pro Audio, best for editing & processing)


🔹 **Example**:
16-bit audio has 65,536 possible volume levels (2¹⁶), while 24-bit audio has 16.7 million levels (2²⁴), allowing for richer sound.
