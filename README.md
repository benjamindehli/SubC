# SubC - Version: [2.0]

A Dreadbox Erebus v2 triangle wave oscillator ran through different saturation circuits and effects.

## Release notes

### Version 2.0 (upcoming)

- Added a plugin version. See the section "The plugin version".
- Fixed the groupIndex in the filter binding.
- Fixed a typo in a keyboard color code.

### Version 1.0 (2024-03-31)

- First version released

## Included formats

- VST3 (macOS, Windows and Linux)
- AU (macOS)
- Standalone application (macOS, Windows and Linux)
- Decent Sampler

## The plugin version

The plugin is a self-contained instrument for macOS, Windows and Linux, available as VST3, AU and Standalone.
Samples, graphics and impulse responses are all embedded in the plugin itself, losslessly compressed, so there are no external files to install or locate.
Only the samples for the selected preset are loaded into memory, and a fresh instance lets you choose which preset to load before anything is decoded.

The plugin has all the controls and features from the Decent Sampler version,including MIDI learn, the master volume fader with output meter, value readouts for the knobs and full DAW automation.
On top of that, the plugin version adds:

- Drift wheels next to the pitch and modulation wheels, adding a subtle random pitch and volume drift to each voice.
- A velocity curve setting in the settings menu.

## Technical specification

|                    | Sample rate | Bit depth | Channels   | Number of files | File size |
| -----------------: | ----------: | --------: | ---------- | --------------: | --------: |
|   **Mono samples** |      48 kHz |    24 bit | 1 (mono)   |             108 | 327.30 MB |
| **Stereo samples** |      48 kHz |    24 bit | 2 (stereo) |             108 | 654.20 MB |

## Instrument presets

- SubC
  - Preset with mono samples
- SubC (Stereo)
  - Preset with stereo samples

## User Interface

| ![Overview](/Screenshots/sub-c.png) |
| :---------------------------------: |
|              Overview               |

### Dynamics

| ![Button controls for the dynamics settings](/Screenshots/dynamics.png) |
| :---------------------------------------------------------------------: |
|                Button controls for the dynamics settings                |

Determines whether the velocity should affect the volume and distortion.

### Saturation

| ![Controls for the saturation settings](/Screenshots/saturation.png) |
| :------------------------------------------------------------------: |
|                 Controls for the saturation settings                 |

The saturation knob blends between the clean samples and the distorted samples.
The clean samples are recorded through a Roland PA-120 mixer.
The distorted/saturated samples are additionally sent through a Hairball Audio FET/RACK (1176 compressor) and a transformer and diode saturator.
The stereo samples are the same as the mono samples, but sent through a TC Electronic SCF Stereo Chorus Flanger in vibrato mode. This gives a much wider sound, but less bottom end when summed to mono.

### Envelope

| ![Controls for the envelope settings](/Screenshots/envelope.png) |
| :--------------------------------------------------------------: |
|                Controls for the envelope settings                |

Shape your sound precisely with the Attack, Decay, Sustain, and Release parameters.
Whether you desire a punchy, staccato tone or a smooth, lingering ambiance, the ADSR envelope allows you to tailor the dynamics to your liking.

## Equipment used

|                                             Name                                             |                                                    Image                                                     |
| :------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------: |
|                           [Dreadbox Erebus v2][Dreadbox Erebus v2]                           |                           ![Dreadbox Erebus v2](/Equipment/dreadbox-erebus-v2.jpg)                           |
|                                [Roland PA-120][Roland PA-120]                                |                                ![Roland PA-120](/Equipment/roland-pa-120.jpg)                                |
|           [Hairball Audio FET/RACK Revision D][Hairball Audio FET/RACK Revision D]           |           ![Hairball Audio FET/RACK Revision D](/Equipment/hairball-audio-fet-rack-revision-d.jpg)           |
| [Alex Franklinos Stereo Transformer Saturator][Alex Franklinos Stereo Transformer Saturator] | ![Alex Franklinos Stereo Transformer Saturator](/Equipment/alex-franklinos-stereo-transformer-saturator.jpg) |
|      [TC Electronic SCF Stereo Chorus Flanger][TC Electronic SCF Stereo Chorus Flanger]      |      ![TC Electronic SCF Stereo Chorus Flanger](/Equipment/tc-electronic-scf-stereo-chorus-flanger.jpg)      |

## About this repository

This repository contains the source for both the Decent Sampler library (the DecentSampler folder) and the plugin version.
The plugin is a thin wrapper around the shared Dehli Musikk sampler engine, and a converter translates the Decent Sampler library into the engine's native preset format at build time.
The audio files are not part of this repository, since the samples are a paid product.
The full version is available from [store.dehlimusikk.no][Gumroad profile].

[Gumroad profile]: https://store.dehlimusikk.no/
[Dreadbox Erebus v2]: https://www.dehlimusikk.no/equipment/instruments/dreadbox-erebus-v2/
[Roland PA-120]: https://www.dehlimusikk.no/posts/ny-mikser-roland-pa-120/
[Hairball Audio FET/RACK Revision D]: https://www.dehlimusikk.no/equipment/effects/hairball-audio-fet-rack-revision-d/
[Alex Franklinos Stereo Transformer Saturator]: https://www.dehlimusikk.no/equipment/effects/alex-franklinos-stereo-transformer-saturator/
[TC Electronic SCF Stereo Chorus Flanger]: https://www.dehlimusikk.no/equipment/effects/tc-electronic-scf-stereo-chorus-flanger/
