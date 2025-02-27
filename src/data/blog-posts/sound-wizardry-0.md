---
title: 🎛️ Sound Wizardry ep.0 - Introduction
publishDate: 26 FEB 2025
description: Introduction to Sound Wizardry.
---

## **🔮 Welcome to Sound Wizardry! 🎶✨**

If you want to **compose music with code**, **design your own audio effects**, or... **create magical sounds** -- welcome to **Sound Wizardry**, journey that will transform you from a complete beginner into an **audio programming wizard**. 🧙🎧

This **series of beginner-friendly** articles will guide you step by step into the world of **sound programming**. Whether you're a total newcomer to the field, or already familiar with programming concepts and want to explore the magic of sound, this series will help you **craft your own sonic spells**.

### 💡 Why Learn Audio Programming?
Audio programming is a vast and fascinating field, used in **video games, music, film** and beyond.
It's where technology, mathematics, and creativity come together to create incredible soundscapes.

Wait, did somoene say... *maths?!* Yes, but don't panic. I will break down the essential concepts
with clear explanations so you will grasp just enough to get productive. 
Also, I will provide optional in-depth resources for those who want to explore further.
Remember: if you want, you can. The most important thing: don't lose curiosity and **have fun**.

**Note.** This isn’t a programming course—it’s a journey into Sound Wizardry. You don’t need coding experience to begin, though it will definitely help.

We live in 2025—AI can explain any code you throw at it. But relying only on AI? That will only take you so far. Real understanding comes from experimenting, breaking things, and figuring them out yourself.

We’ll start with Python. There are tons of free courses and resources out there—just pick one that looks fun and dive in.

Yes, serious audio programming involves **C++** (or other lower-level languages), but don’t worry about that right now. We’ll get there when the time is right. 

**Okay, so we have all disclaimers in place, now let's dive in and begin with...**
<hr>

## 🌟 Casting Your First Sound Spell
...or, running your first Python program.

### 🖥️ Step 1: Installing Python
Before we write any code, we need *Python* installed on your computer. I assume that if you are a person
on the internet, you're likely a *Windows* or *Mac* user. 
There's tons of tutorials about it out there, so I won't waste our time on it. Do it any way you find 
most comfortable for you.

### 🔹 Step 2: Set Up Visual Studio Code
We'll be writing and running our Python programs using **Visual Studio Code (VS Code)**.
Why? Because it's simple, beginner-friendly and easy to use. If you want to run your programs in any other
IDE, feel free to do so.

1. Download and install [VS Code](https://code.visualstudio.com/Download)
2. Open **VS Code** and install the **Python extension** (search for "Python" in the *Extensions Marketplace*).
3. Open a new folder where you'll store your sound projects.

## 📦 Step 3: Install Sound Libraries
For starter, we'll be using two libraries to play our sounds: `sounddevice` and `numpy`.

1. Open *Terminal* in your **VS Code**. Make sure you [use **Bash**](https://stackoverflow.com/a/50527994).
2. Run command:
```bash
pip install sounddevice numpy
```

## 🎹 Step 4: Write Your First Sound Program
...or copy-paste it. It will also work...

🔹 **In VS Code, create a new file called "beep.py" and copy in this code**:

```python
import numpy as np
import sounddevice as sd

# Generate a simple beep (440 Hz for 1 second)
frequency = 440  # A4 note
duration = 1.0   # seconds
sample_rate = 44100  

t = np.linspace(0, duration, int(sample_rate * duration), False)
wave = 0.5 * np.sin(2 * np.pi * frequency * t)

sd.play(wave, samplerate=sample_rate)
sd.wait()
```

## 🚀 Step 5: Run Your Code
Open your terminal in **VS Code** again, and run your program using:
```bash
python beep.py
```

## 🎶 Beep!
🎉 You should hear a beep sound! If you do, congratulations—you just wrote and ran your first **Sound Wizardry** program. 

You can play around with the duration and frequency, but turn down your volume and preferably don't use headphones... If you mess up and want to stop the sound, simply panic and spam **ALT+F4** as fast possible (or unplug your computer). I swear our next programs will not be that trash...

If you're ready, you can go to the next chapter - [**The Building Blocks of Sound**](/blog/sound-wizardry-1).

