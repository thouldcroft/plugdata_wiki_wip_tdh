# DAW Integration - Ardour

## Creating and Editing Patches
Ardour is one of the DAWs that may not register the typing keyboard for creating and editing objects in plugdata. To enable keyboard input:
- Click on the keyboard icon in the upper right corner of the plugin window:

    ![Ardour](../images/ardour-screenie.png)


## MIDI In

1. Add **plugdata** as an instrument to an empty MIDI track.
2. In **plugdata**, use one of the MIDI IN objects and route MIDI data from it *(see example)*.
3. Play notes on this MIDI track using any usual method — keyboard, piano roll, etc.

![live-midiin](../images/pd-midiin.png)

## MIDI Out

![ardour-midiout](../images/ardour-midiout.png)

1. Add **plugdata** as an instrument to an empty MIDI track.
2. In the **Editor Mixer** (*Shift-E* to toggle) for the **plugdata** track, add an instrument which will receive MIDI data, right below the **plugdata** plugin *(a)*.
3. In **plugdata** plugin, use one of the objects that sends out MIDI data *(see examples)*.

![pd-midi](../images/pd-midiout.png)

## FX

1. Add **plugdata-fx** as an effect device to an audio or MIDI track.
2. In **plugdata**, use [adc~] object to receive audio from your DAW *(see examples)*.  

![live-a3](../images/pd-fx.png)