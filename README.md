# shadydrummer~.pd
![shadydrummer~snapshot](https://i.imgur.com/j9wB29L.png)

# Table of Contents
1. [Overview](#overview)
2. [Installation](#installation)
3. [Features](#features)
4. [Customization](#customization)
<br><br>

# Overview
shadydrummer~ is a sample-based drum sequencer patch. To program a drum sequence, simply click on the blocks at desired beats to trigger each piece of the kit. To output audio from the patch, create a "catch~ drum-sum" object and connect to dac~.
<br><br>

# Installation
Copy all patches and the /sample folder into a directory added to Pd, then instantiate by creating a "shadydrummer~" object in any patch.

*NOTE: patch will not work without helper patches "sipmlecolortog.pd" and "colortog.pd", they will need to be put in the same directory where shadydrummer~ exists.
<br><br>

# Features
**Library Selection**<br>
shadydrummer~ comes with 4 sets of drumkit sounds, use the horizontal radio bar to select a kit.<br>

**BPM**<br>
To change the BPM, use the number box at the top. A max value of 208 bpm has been set to ensure optimal listening experience.

**Presets**<br>
It is possible to create presets in shadydrummer~ through bang messages. Create a message object, and specify the blocks you would like triggered in the preset with the following format: `on-row#-column# 1;` where row# represents the piece in the kit (top-down 1 through 8) and column# represents the beat (left-right 1 through 16).

A bang message should look like this:
```
;
drumon 0;
on-1-1 1;
on-1-3 1;
on-4-5 1;
```
An working example can be found inside the "shadydrummer~" patch as well.<br><br>

# Customization
Sounds in the /sample folder can be swapped out by replacing the original file with another file or by renaming the new file to match the target replacement.<br><br>

# Acknowledgements
This patch was originally inspired by mrp805's [Pure Data Sequencer 2015](https://youtu.be/9Nz0bxwoqQE), and created with the help of Prof. Miller Puckette and Dr. Kevin Haywood at University of California, San Diego.