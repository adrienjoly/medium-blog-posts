---
title: How to configure the HH65 hi-hat pedal on Yamaha DTX Multi-12
date: '2019-06-02T14:57:47.352Z'
subtitle: "I.e. Make the hi-hat pad of the “Oak Custom” kit sound “opened” unless you press the\_pedal."
excerpt: >-
  I.e. Make the hi-hat pad of the “Oak Custom” kit sound “opened” unless you
  press the pedal.
thumb_img_path: >-
  images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*DgDHFlOyiY3LdprW.jpg
layout: post
---
Hi!

By default, when you hit pad 9 with the built-in “Oak Custom” kit, the DTX will play a “closed” hi-hat sound. That’s a great default setting when you want to play without pedal, as you can use pad 12 to play the “opened” hi-hat.

When plugging the HH65 hi-hat pedal into the “HH CTRL” port of my DTX for the first time, I was surprised to see that the behavior of pad 9 remained unchanged. With the DTX default settings, the HH65 was useless.

Here are the steps I had to follow in order to make pad 9 play an “open hi-hat” sounds by default, and use the HH65 pedal to “close” it. This guide was inspired by the following video:

### Step 0. Backup your kit

It may sound obvious, but I recommend that you make a copy of the “Oak Custom” kit, and name it “Oak HH65”. (you can do that from menu KIT-2-3-1)

### Step 1. Set the A and C layers of pad 9

Press the “MIDI” button, then hit pad 9 to select it.

Make sure that “MessageType” is set to “note”.

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*DgDHFlOyiY3LdprW.jpg)

When it’s done, press “Enter”.

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*ECW7b7ItCikOqj6g.jpg)

This will lead you to the “MIDI1–1” section.

Still for pad 9, select the “stack” mode.

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*fAI8lPjbzAFxe5PW.jpg)

Press the “>” (right) button to go to the second page of that section. (“MIDI1–2”)

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*V3Gh8cUcuwVE63bF.jpg)

On the “A” layer of pad 9, pick the “A#1 / 46” note (instead of “F#1 / 42”).

Use the “ 🔻🔺” (down/up) then “>” (right) buttons to select the “C” layer.

On the “C” layer of pad 9, pick the “F#1 / 42” note (instead of “A#1 / 46”).

For layers “B” and “D”, leave the Note “off”.

Don’t forget to press “STORE” and confirm in order to save your changes.

### Step 2. Set the voices

Now that MIDI layers and notes are setup for both positions of the pedal, let’s pick the sounds that will be played by the DTX when hitting those notes.

In order to do that, press the “VOICE” button, and make sure that pad 9 is selected.

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*tbbI9U5_qXgKrB09.jpg)

While navigating similarly to what we did in the previous step, map:

*   Layer “A” of pad 9 to “HH001:Brite Op” (opened hi-hat)
*   Layer “C” of pad 9 to “HH005:Brite Cl” (closed hi-hat)
*   The “HHCL” pad (push the pedal) to “HH003:Brite FtCl” (foot close)
*   The “HHSP” pad (use arrow buttons) to “HH004:Brite FtOp” (foot open / splash)

Don’t forget to press “STORE” and confirm in order to save your changes.

### Step 3. Enable “Hi-Hat” layer switching

Press “KIT” and navigate to the “Other” section using the “>” (right) button.

After pressing ENTER, set “LayerSwitch” to “hh”, still on pad 9.

![](/images/How-to-configure-the-HH65-hi-hat-pedal-on-Yamaha-DTX-Multi-12/0*U_qO5ycdew7pWXVg.jpg)

Don’t forget to press “STORE” and confirm in order to save your changes.

### Enjoy!

With these settings, you should be able to enjoy a more realistic drumming experience with your DTX and hi-hat pedal, both using the sound generator of the DTX and your favorite DAW, thru MIDI. (The pedal also worked as expected when I plugged the DTX to GarageBands, for instance.)
