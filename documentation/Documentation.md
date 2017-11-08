## Crescendo 2   ##

This document details functionality of models of Crescendo 2 . The goal is to provide an easy to use interface utilizing the latest Smart Graphics.

The user experience should be consistent across all interfaces.

----------

### Climate ###

To configure climate modules in your system:
1 - Add one module Climates (99% without configurations)
2 - Add one module Crestron CHV-THSTAT for each internal equipament of Air Conditionate ( If you have a room with 2 AC, you need add 2 modules)
3 - Configure this module:
	- Name -> Unique name thar indicate the AC, normaly is room name
	- ID -> First module is 01, incremente by 1 for other modules.
	- Set Point Type -> If the AC need two separated set point ( Low and Hight, Cool and Heat) set to Double Set Point ( This will show two adjusts in panels), or if is AC Split that need one set point, set to Single Set Point ( This will show only one adjust in panels).
    IN This module that you will conect the drives do AC equipament ( IR driver, etc.)


----------


### Shades ###

To configure shades modules in your system:
1 - Add one module Shades (99% without configurations)
2 - Add one module Shade for Room( You can control up to 12 shade/curtain with same module, with independent controls)
3 - Configure this module:
	- Name -> Unique name of room 
	- ID -> First module is 01, incremente by 1 for other modules.
	- Shade Name (1 to 12) -> Name of shade/curtain (Ex. Left, Right, Shade, etc.)
	- Shade Type (1 to 12) -> Select onde type (Left Curtain, Two Curtain, Right Curtain or Shade), this only change the desingn of shade in interfaces.
    IN This module that you will conect the drives do  shade/curtain ( IR driver, C2N-SDC, C2N-SSC,etc.)


----------



### Lights ###

To configure lights modules in your system:
1 - Add one module Lights (99% without configurations)
2 - Add one module Light for Room ( You can control up to 15 zones/channels Dimmered or on off with same module, with independent controls). 
3 - Configure this module:
	- Name -> Unique name of room
	- ID -> First module is 01, incremente by 1 for other modules.
	- Button Label (1 to 15) -> Name of Button/Preset(Ex. Left, By, Night, etc.)
	- Channel Type (1 to 15) -> Select onde type Dimmer or OnOff (this show slider or on off button in interface).
	- Channel Name (1 to 15) -_ Name of Channel/Zone of eletric circuits (Ex. Front, Left, Closet, etc.)
	- Hold Time - Time in seconds that you need  hold the button to save a lights cene (ex. 5s)
	- Fade Time  - Time in seconds that a dimmered channel/zone delay to change of level ( ex 5s to go of on to off)
	If you connect [press_01] to preset1 the button 1 will be a preset cene 1, to save a cene, press for "hold time" seconds and the indicator will flash 5 times to indicate thar cene was save.
	If you channel/zone is on off user light1_on_off to control it, else if is dimmered use analogic zone1_level to control the zone, and zone1_feedback to receiva a fb of zone.


----------

Shutdown
[All Home Off Close] - Close all shades, off climate, off Multimidia, off al lights of home.
[All Room A/V Off  ] - Power off all Multimidias of home.
[Room Off Close    ] - Close all shades, off climate, off Multimidia, off al lights of room.
( Multimidia Room Off) - Power off multimidia of room.



