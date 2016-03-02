## Crescendo 2 Demo: Scope of Work ##

This document details functionality requirements for the Crescendo 2 Demo system. The goal is to provide an easy to use interface utilizing the latest Smart Graphics.

The user experience should be consistent across all interfaces.

----------

### System Overview ###

#### "The Loft" ####

**Global:**
(2) iPads and (2) iPhones provide roaming (and external) access for all rooms and system features.

**Media Room:** Powered by a Crestron DM6x4 switcher along with a _Crestron Connected_ A/V receiver.

_Primary Interfaces:_ iPad, TSR-302.

**Kitchen:**
The Kitchen television has access to Media Room sources via the second output of the DM6x4. _(Kitchen video sources will provide audio through the television speakers, audio sources will route through ceiling speakers.)_

HR-150 contains a "Media" button that will synchronize with what is being watched in the Media Room _(if the overhead speakers are on, they should turn off.)_

_Primary Interfaces:_ TSW-750, HR-150.

**Master Bedroom**

The Master Bedroom includes local video with a Tivo Mini (sharing with the Media Room's Genie) and Apple TV. Sound for the video system is provided by a Sonos Playbar _(audio sources are routed to ceiling speakers)._

_Primary Interfaces:_ HR-150, iPhone, iPad.

**Environmental:** the system includes wireless lighting and shade control for the main area and 2 wired thermostats. 


----------


### Components ###

- **Audio Distribution** `Crestron Sonnex 24x8`
	- Source: Crestron NSP-1
	- Source: Airplay (2-channel digital audio from AppleTV)
	- Source: Sonos Connect _(mobile devices should provide option for app launch)_
- **Video Distribution** `Crestron HDMD-6x2`
	- Source: Tivo Genie (TCP/IP)
	- Source: AppleTV (IR)
	- Source: Sony Blu-ray (IR)
	- Source: XBOX (input only)
- **Local Sources**
	- Tivo Mini _(Master Bedroom)_
	- Sony SmartTV features _(Master Bedroom)_
- **Interfaces**
	- `iPad` (2): Global interface to control all system functions.
	- `TSR-302` (1): Remote control for Media Room including thermostat, lighting, and shade control.
	- `TSW-750` (1): Primary interface for Music and Lighting control in the Kitchen.
	- `HR-150` (2): Remote control for Kitchen and Master Bedroom. _(Select Video and Audio sources, the user should have appropriate volume control depending on the source they have selected and be able to have the TV on in the background while music plays through the overhead speakers.)
	- `iPhone` (1): The iPhone should control all system functions. The primary purpose is remote system connection for environment control, however the client does want the ability to use the phone as an A/V controller.
- **Lighting** 
	- `D3Pro` Virtual keypad support. _Lights must by dynamically programmed so that buttons and keypads can be added to the lighting system without loading graphics files._
- **Thermostats** 
	- (2) Wired Crestron CHV-TSTAT.
- **Shades**
	- PYNG (integrate with existing PYNG Shades.)

### Source Code ###

Full source code must be provided with a documentation reference and an open license for future changes. The program should compile without warnings or notices.