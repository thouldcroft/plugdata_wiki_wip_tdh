## Audio

![adc_dac](../images/adc_dac.png)

The [adc~] and [dac~] objects are used to handle audio IO, both in the standalone and the plugin version. Make sure DSP is enabled, and the master volume is on.

![audio on](../images/audio_on.png)

If you are using the standalone and you don't get any audio IO, check your audio settings in the settings panel.

![settings menu](../images/settings.png)

![settings](../images/settings_dialog.png)


## Communicating with the DAW

![DAW comms](../images/daw_comms.png)

The [param] object is used to send/receive DAW automation. It takes one argument, the index of the parameter you want to send/receive. You can also create a [param] object from the automation panel.

![paramters](../images/params.png)

The [playhead] object can be used to receive information about the current position of the DAW's playhead. It also passes on various other information, such as BPM, time signature, loop status and more.

For more information about [param] and [playhead], right click on the object and select "Help".


