Abstractions by João Pais

Version 0.61

(c) 2005-2021 João Pais - jmmmpais@gmail.com
Released under the BSD and CC A-NC3 licenses (more information in each abstraction).


This package has several utilities with different functions. It is composed of abstractions only.

ardourjack-gui	Controls ardour transport and jack settings from Pd
array-edit	Edit properties of arrays and populate them following several formulas
bezier	Transfer function GUI with one cubic bézier curve
bezier~	Transfer function GUI with one cubic bézier curve at audio rate
but	Monochrome bang button
butt	Color-changing Toggle Button
cellblock	numeric grid
change-symbol	like vanilla's change, but for symbols
clock	Chronometer with display in seconds
dacc~	dynamic dac~ outlet up to 32 channels
dacm~	Mono dac~ for lazy people
datei-o	Sends the message "open ../../"
datei-r	Sends the message "read ../../"
datei-w	Sends the message "write ../../"
ds-color-sel	color selector for data structures
dsp01	DSP switch
f+	Counter with variable increment
Granulator	Pure Data port of Robert Henke's Granulator
gui-edit	edit standard GUI objects fast
jp.coll	store/edit message collections VERY SIMILAR to cyclone/coll, but in vanilla
jp.dbtofad	a vanilla modelling of [iemlib/dbtofad]
jp.garble	garble Pd patches
jp.list-drip	similar to other versions of list-drip
jp.menu	Dropdown menu programmed with data structures
jp.preset	Dropdown preset saver programmed with data structures
jp.sigtovu~	signal to rms converter in VU meter format
jp.split-symb-first	split a symbol, using a character as separator.
jp.split-symb-last	split a symbol, using a character as separator.
jp.symbol-expand	split a symbol into a list with individual elements separated by spaces
jp.urn	unrepeated random numbers. As in the cyclone object but in vanilla.
LANPdini	attempt to port J. Narveson's LANdini to Pd
lbang	loadbang which can be triggered more often
liner~	practical implementation of [line~]
liner+~	practical implementation of signal envelopping
live2reaper - Synchronizer from Ableton Live to Cuckos Reaper, though Ableton Link.
mat~	Level meter with amplitude control
mat-~	Level meter with amplitude control, horizontal
maat~	Level meter with amplitude control, stereo
maat-~	Level meter with amplitude control, stereo, horizontal
mat4~	Level meter with amplitude control, 4 channels
mat4-~	Level meter with amplitude control, 4 channels, horizontal
matrixctrl	GUI for [iemmatrix/mtx_mul~]
met~	Level meter with amplitude control (with VU, too CPU expensive for me)
metrum	Metro with GUI
m-i	Automatic conversion of MIDI controller
mk	Visual display of MIDI inputs
multiarray	store and operate several graphical arrays in one graphical container
oscD	Counts received OSC messages
oscS	Interface for sendOSC
pd-colors	Pd color palettes (Data Structures + Tcl/Tk)
pix2canvas	Convert images into canvas
rec-name	Automatic naming for a record/playback engine
rgb-color	Pick RGB colors for your GUI objects
scale	maps an input range to an output range, in vanilla
sguigot	spigot GUI implementation
sliders	GUI for incoming midi data
snaps~	snapshot~ GUI implementation
spectrogram~	Spectrogram with 512 bins resolution
stoppuhr	Chronometer with two layers
swatch	Pick a color using the hue-saturation chart
swatch-gui	Pick a color for your GUI using the hue-saturation chart
tastin	Gate for keyboard input
uhr	Shows the time


The jmmmp library is dependent from the following libraries: ceammc, cyclone, ext13, ggee, iemlib, iemmatrix, zexy (and maybe others).

2021.05.24


Non-working or discarded abstractions:

aufnahme~ - Multichannel audio recorder (1 to 8 channels)
bcf2000 - Store and recall presets for Behringer BCF2000
-dsp - replaced by dsp01
datei-l - replaced with datei-o


CHANGELOG

Version 0.61
- added [change-symbol], [jp.urn] and [shuffle]
- added "coll.init" method to [jp.coll]
- fixed a bug in [Granulator] and with increment in [f+]
- [snaps~] right inlet change
- changed declare -stdlib and -stdpath to -lib and -path in all objects to conform to better practices

Version 0.60
- added [jp.coll]

Version 0.59
- added [live2reaper]

Version 0.58
- added [cellblock] and [scale]
- added list-abs dependency to [matrixctrl]

Version 0.57
- added [jp.garble], [jp.list-drip], [jp.split-symb-first], [jp.split-symb-last], [jp.symbol-expand]
- removed some external dependencies from [swatch] and [swatch-gui]
- improved external declarations for [ardourjack-gui], [array-edit], [bezier], [bezier~], [dacm~], [jp.menu], [jp.preset], [sliders], [stoppuhr]
Features added to [multiarray]:
- improved display of audio arrays
- "write" output message
- removed code redundancies
- added patch cleanup after saving
- x-display
- get color, thickness, vis
- y-axis reference line

Version 0.56
- removed some pddp dependencies
Features added to [multiarray]:
- show ID
- y-window scaling
- fixed a bug in "size" method
- read and write audio files
- configuration file to load at startup 
- background
- general setting for color, thickness, visibility

Version 0.55
Features added to [multiarray]:
- removed dependency from iemguts and multiarray-unit.pd external
- array visibility
- ID check and ID status query
- save and load multiarray data
- x and y scaling

Version 0.54
- Added [multiarray] and [jp.sigtovu~]

Version 0.53
- Added [jp.dbtofad], [mat4~] and [mat4-~]
- fixed iemlib dependency in [matxxx~] objects.

Version 0.52
- [jp.menu] and [jp.preset] - changed donecanvasdialog command to coords, because of vanilla bug going into edit mode.
- [Granulator] - fixed bug that activated FM modulation
- [mat~] object group - included color display for signal volume


A FAZER
- jp.menu, jp.preset, e outros com seleccao de cor data-s - seleccao actualiza o display automaticamente. Ver se nao há problemas com inputs que já existem.
- bug com último preset em jp.preset. substituir msgfile e outros por vanilla?
- acabar [LANPdini]