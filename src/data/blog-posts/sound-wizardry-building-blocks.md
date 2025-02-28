---
title: 🎛️ Sound Wizardry - Building Blocks of Sound
publishDate: 28 FEB 2025
description: What do we need to represent a sound in our computer?
---

#### **🔮 Welcome to Sound Wizardry! 🎶✨**

This is a series of articles designed to tackle key Audio Programming concepts in accessible and engaging way. 
Whether you're learning from scratch or brushing up on the fundamentals, there’s something here for you. If it's your first time here,
check out the [Introduction](/blog/sound-wizardry-introduction).

## 🌟 Introduction
This one will be more theoretical than practical, but I think interesting for pretty much everyone!

In this article, we will answer the question: what do we even need to represent a sound in our computer?


## 🎵 Frequency (Pitch) - The "Note" of Sound
When your favorite musician plucks his guitar, the vibrations of the strings produce sound waves.
Those waves travel thorugh the air at a certain *frequency*. Through your ears, they enter your brain as signals,
that are "decoded" and perceived by you as sound of a specific *pitch*.

You may notice in the header that I put *pitch* in parentheses near *frequency*. Those two concepts are very closely related,
and for our purposes we can think of them as the same thing. Just for the record though,
- **frequency** -- is an objectively measured physical characteristic,
- **pitch** -- is a mental representation of *frequency* in our minds.

The concept of frequency is straightforward: the slower something vibrates, the lower its frequency.
We perceive lower frequencies as deep, bass sounds, and higher frequencies as sharp, treble sounds, like those form a whistle.

When you played your flute in 3rd grade, by covering the instrument’s tone holes, you made the air travel a longer distance. This slowed down the vibrations of the air inside the flute, creating a lower sound.

#### 📋 Here are a couple of facts about **frequency** to remember:
- Measured in **Hertz (Hz)**
- **Low frequency** = **Deep/Bass sounds** (e.g., 60 Hz = subwoofer rumble)
- **High frequency** = **Sharp/Treble sounds** (e.g., 5000 Hz - whistle)
- 🔹 **Examples on piano**: 
  - **261.6Hz** - note **C4**, the middle C key on a piano
  - **246.9Hz** - note **B4**, the key to its left.
- The human hearing range is **20Hz - 20,000 Hz**. We are *physically incapable* to hear higher frequencies. 
  - Shame, we can't hear our dogs whistles...
    - On second thought, maybe it's better that way.

## 🔊 Amplitude (Loudness) - The Volume of Sound
The amplitude of sound waves refers to the maximum displacement of parti... well who cares,
if you want physical definition - check it out [here](https://en.wikipedia.org/wiki/Amplitude).

For our purposes, it's enough that you know that *amplitude* refers to the strength, or intensity of a sound wave.
In digital audio, it determines the **loudness of the sound**.

#### 📋 Here are a couple of facts about **amplitude** to remember:
- Measured in **Decibels (dB)** (a logarithmic scale of loudness)
- **Higher amplitude** = **Louder sound**
- **Lower amplitude** = **Quieter sound**
  - Whispering is about 30 dB, while a jet engine is 120 dB.
- In digital audio, amplitude is usually represented in range of **-1** to **1** (normalized).

## 📈 Waveforms - The Shape of Sound

Dark mode users - sorry for my laziness, but this would work best if you scroll up and toggle light mode of the website for a second... I just don't have a better image. <p style="font-size: 12px; margin-top: -30px;"><i>to be honest I wasn't looking for any.</i></p>
<img src="/assets/blog/sound-wizardry/Waveforms.png" width="400" alt="black sabbath" style="margin-left:50%; transform: translateX(-50%);" />
<p style="text-align:center; font-size: 12px"><i>Fig. 1 - Example waveform shapes</i></p>

The lines on the chart represent how a sound wave is captured and stored by a digital device.

Here’s how it works:
- 🔹 **Sound is a continuous wave in the air** → a microphone picks up vibrations.
- 🔹 **The device records points at regular intervals** (***sampling*** - *more on that in the future)* → these are data points that show the wave’s amplitude at specific times.
- 🔹 **The lines connect these points** → forming a visual representation of the sound wave

Sound has three key ingredients, and now we are getting the final building block:
1. **Frequency** - how quickly the pattern repeats - **Pitch**!
2. **Amplitude** - how tall the wave is - **Loudness**!
3. **Waveform** - the shape of the pattern...

...well, what does the shape of the wave tell us?

It's the **tone**. The note **C4**, played both on a piano and a guitar, is considered the same note. 
It does indeed have the same frequency, and may have the same amplitude. So why can we tell whether it was played
on a guitar or on a piano? <p style="font-size: 12px; margin-top: -30px;"><i>(or coughed by some dude in the bus)</i></p>

That exactly what the shape of the wave tells us. Even if two sounds have the same **frequency** (same note) and **amplitude** (same loudness), they can still sound completely different because of their **shape**!

> By the way - all that doesn’t just apply to sound. <br/>
>Similar concepts relate to pretty much any periodic wave in nature, like light waves, radio waves, and even ocean waves. <br/>
> You definitely seen those concepts somewhere in your schooling journey already (*although whether
> you were paying attention is a different story*.)

Here's a quick description of how those waveforms from chart above sound:
- 🔷 **Sine Wave (Pure Tone)** – Soft and smooth (e.g., tuning fork)
- 🔷 **Square Wave** – Harsh, buzzy sound (used in retro game music)
- 🔷 **Triangle Wave** – Softer than a square wave, more flute-like
- 🔷 **Sawtooth Wave** – Bright and sharp, used in synthesizers

Let's generate and hear them on our own!
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
Change `"sawtooth"` to `"sine"`, `"square"`, or `"triangle"` and hear the difference.

## Some technical stuff for ending
We’ve covered a lot of what might seem like basic concepts, but in reality, these ideas can take time to fully sink in.
They’re not as simple as they might appear, so don’t worry if you need to revisit them later,
look up other resources, or even ask your favorite AI buddy for help.

If you feel ready, let's move to last two concepts that I wanted to touch on.

## 🎧 Sample Rate - How Often We Capture Sound
At some point, as a curious human being, you've probably come across numbers like
44,100 Hz, 48,000 Hz, 96,000 Hz, or heard terms like CD Quality, Studio Quality, etc. But what does it all mean?

**Sample rate** is measured in *samples per second* (**Hz**). It tells us, how often the device that we've been using
to record our sound **sampled** (*captured*) the sound. 

- **44,100 Hz** means 44,100 samples per second, which is the standard for CD quality audio.
- **48,000 Hz** is common for video production and some studio recordings.
- **96,000 Hz** is used for high-quality studio recordings, offering more detail and clarity, but it also creates larger file sizes.

The higher the sample rate, the more accurate the recording, but it comes at the cost of bigger files.
**Sample rate** plays a crucial role in how well we capture and reproduce both details of loudness (amplitude) and high-pitched sounds (frequency). Higher sample rates give us more detail and accuracy across all frequencies, resulting in better sound quality overall.
> A higher sample rate is like a high-frame-rate video<br/>—smoother, more detailed sound.

## Bit Depth - The Detail in Sound
First off, thanks for sticking in! We've covered a lot of ground, and this is the last concept. The **Bit Depth**.
Maybe you ever wondered what **16-bit** (CD Quality), **24-bit** (Studio Quality), **32-bit** (Pro Audio) means?

It simply controls the **resolution** - how accurately we store *amplitude levels* (loudness) of a sound wave.
It determines how many possible volume levels w ecan use to represent a sound's loudness at any given moment, like the **precision** with which we measure the sound's volume.

For example:
- **16-bit** audio has **65,536** possible volume levels (2^16),
- **24-bit** audio has **16.7 million levels** (2^24), allowing for richer sound.
- **32-bit** audio has over **4 billion** levels. While not typically used for the final listening formats, allows for super precise adjustments without losing any audio quality

Lower bit depth has its limits when it comes to *extremely quiet or* *loud* sounds. Works for most everyday listening situations
like CD, but professional music production requires capturing very subtle changes in volume.

## Summary

Thank you for reading. We've covered a lot of essential audio programming concepts, from understanding how **frequency** (*pitch*) and **amplitude** (*loudness*) shape sound, to exploring the **waveform** (*tone*) and its importance. We also looked into how **sample rate** affects how often we capture sound and how **bit depth** determines the precision of loudness in sound recordings.

Sound has three key ingredients: 
- **frequency** (pitch), 
- **amplitude** (loudness), 
- and **waveform** (tone), 

which come together to create the full experience of audio. We also discussed how higher sample rates and bit depths provide more detail and accuracy in sound, allowing for higher-quality recordings.

I hope you found something useful here. These concepts might take time to fully sink in, so don’t hesitate to revisit them whenever needed.

See you in the next one! 🎶✨