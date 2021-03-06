# granularFX
Granular Effects in Supercollider

[Demo](https://vimeo.com/684535902)

![GUI](gui.png?raw=true "granularFX")

## Prerequisites
* Install [Supercollider](https://supercollider.github.io/download)
* Install sc3-plugins
  * Download [sc3-plugins-3.11.1-macOS-signed.zip](https://github.com/supercollider/sc3-plugins/releases/download/Version-3.11.1/sc3-plugins-3.11.1-macOS-signed.zip) and unzip.
  * Move the contents of the unzipped `SC3plugins` directory to `"$HOME/Library/Application Support/SuperCollider/Extensions"`

## Install

*Install granularFX as an extension*

Perform this step once everytime `granularFXClasses.sc` is updated.

* Open `setup.scd` in Supercollider and execute following commands from the menu
  * `Language -> Evaluate File` (or Command-Return `⌘ ↩`)
  * `Language -> Recompile Class Library` (or Shift-Command-L `⇧ ⌘ L`)

## Launch GUI

* Open `granularFX.scd` in Supercollider and execute following commands from the menu
  * `Language -> Evaluate File` (or Command-Return `⌘ ↩`)

## Usage

* Select suitable Input and Output Devices
* Turn on granulators and adjust the dry/wet mix
* `⌘ .` to exit

## Troubleshooting

* Supercollider complains that "Mismatched sample rates are not supported" and refuses to boot up
  * This may be the case if one of the available input audio devices does not support the same sample rate as the default output device.
  * To circumvent this, before running `granularFX.scd` please specify the in/out devices you intend to use in [`Line 15 & 16`](https://github.com/avroshk/granularFX/blob/main/granularFX.scd#L15-L16). Here's an example,
  ```
  var inDevice = "BlackHole 16ch";
  var outDevice = "Built-in Output";
  ```
  * The input and output devices specified above should operate on same sample rates. You can check `Audio MIDI Setup` to verify this.

### More reference material
* https://pustota.basislager.org/_/sc-help/Help/Tutorials/Buffer_Granulation.html
