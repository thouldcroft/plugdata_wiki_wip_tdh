# Compilation and Integration with HVCC Compiler

## Overview

**plugdata** provides functionality for patches to be compiled for various targets. The supported targets are:

- **C++ code**: Generates C/C++ source code for use in other DSP projects.
	
- **Electro-Smith Daisy**: Compiles and flashes code onto a (Daisy)[https://electro-smith.com/] microcontroller board and related devices.

- **DPF Audio Plugin**: Creates an audio plugin for use in various plugin hosts.

- **Pd External**: Compiles into a Pure Data external object, optimizing its performance.

WARNING: The destination path for exporting code or plugin binaries must not contain spaces.

## Compiled Mode

In the main plugdata menu, you will find a toggle box labelled **Compiled Mode**. This mode checks your patch for compliance with plugdata compilation tools. It uses the [Heavy hvcc compiler](https://wasted-audio.github.io/hvcc/docs/01.introduction.html#what-is-heavy), which can generate code for a subset of Pure Data Vanilla objects. By downloading the compilation toolchain, the Heavy hvcc compiler maintained by [Wasted Audio](https://wasted.audio/) will be installed, along with additional compilation utilities.

**Compiled Mode** indicates if there are objects in your patch that cannot be used in a compiled patch by posting a message to the console, and outlining the object in question. The auto-completion in plugdata will also only provide compatible objects when this mode is activated.

Object error indication when using an unsupported object in Compilation Mode:
![heavy object unsupported](../screenshots/heavy_unsupported.png)

Console error warning when using an unsupported object in Compilation Mode:

![heavy console warning](../screenshots/heavy_unsupported_warning.png)

## Compiling in plugdata

Selecting `Compile...` opens a window with compilation options for different modes, each with common and mode-specific configurations.

### General Configuration

![heavy general config](../screenshots/heavy_general_config.png)

Common fields in this section include:

* **Patch to export**: Choose the patch you wish to export.
* **Project Name (Optional)**: Autofills with the patch's name.
* **Project Copyright (Optional)**: Specify under one of the [common source licenses](https://spdx.org/licenses/).

### C++ Code

![heavy cpp menu](../screenshots/heavy_cpp_menu.png)

In C++ Code mode, your plugdata patch is transpiled to generic C/C++ code. Adapt the raw code for specific applications. Learn more in the [official documentation](https://wasted-audio.github.io/hvcc/docs/05.c.html).

### Electro-Smith Daisy

![heavy daisy menu](../screenshots/heavy_daisy_menu.png)

Daisy mode allows running your patch on an embedded hardware device based on an STM32 microcontroller. Options include choosing a target board, export types (Source Code, Binary, Flash), enabling USB MIDI, and configuring patch size.

### DPF AUdio Plugin

![heavy dpf menu](../screenshots/heavy_dpf_menu.png)

DPF mode exports self-contained versions of your patch in various formats (VST2, VST3, LV2, CLAP, JACK). Choose export type (Source Code, Binary) and plugin type (Effect, Instrument, Custom). Select plugin formats in the provided list.

> When compiling *DPF Audio Plug-ins*, patches cannot contain any special characters: <br>
		` ~ @ ! $ # ^ * % & ( ) [ ] { } < > + = _ – | / \ ; : ' “ , . ?

### Pd External

![heavy pdexternal menu](../screenshots/heavy_pdexternal_menu.png)

Export your patch as a Pd external for optimized performance. Choose export type (Binary or Source Code) and enable copying to the externals path.

Refer to the [official documentation](https://wasted-audio.github.io/hvcc/docs/03.gen.pdext.html) for more details on each export option.

