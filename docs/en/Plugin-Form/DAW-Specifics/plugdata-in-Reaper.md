# DAW Integration - Reaper

## Creating and Editing Patches
Ardour is one of the DAWs that may not register the typing keyboard for creating and editing objects in plugdata. To enable keyboard input:
- Enable the "Send all keyboard input to plug-in" option in the FX menu of the plugin window:

    ![REAPER](../../../images/reaper-screenie.png)

## MIDI In
1. Add **plugdata** to an empty track.
2. In **plugdata**, use one of the MIDI IN objects and route MIDI data from it *(see example)*.
3. Play notes on this MIDI track using any usual method — keyboard, piano roll, etc.

![reaper-midiin](../../../images/pd-midiin.png)

## MIDI Out

![reaper-midiout](../../../images/reaper-midiout.png)

1. Add **plugdata** to an empty track *(a)*.
2. In **plugdata**, use one of the objects that sends out MIDI data *(see examples)*
3. Add another track. We'll call it RECEIVER *(b)*. Load an instrument that you want to receive MIDI from **plugdata** on this track.
4. Click and drag the Route button of the **plugdata** track *(c1)* to the Route button of the RECEIVER track *(c2)*.

![pd-midi](../../../images/pd-midiout.png)

## FX
1. Add **plugdata-fx** as an effect device to an audio or MIDI track.
2. In **plugdata**, use [adc~] object to receive audio from your DAW *(see examples)*.

![reaper-fx](../../../images/pd-fx.png)
