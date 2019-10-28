# Crescendo Framework 2.1.91

Crescendo is the only free and open-source software framework for Crestron control systems. Crescendo is designed by [Adelyte Company](https://www.adelyte.com/) and maintained by the company and the community. Please visit the [project page](https://www.adelyte.com/crestron/crescendo) and [documentation](https://www.adelyte.com/crestron/crescendo/docs) for more information.

## Getting Started

[Crescendo 2 "The Loft" Walkthrough](https://vimeo.com/193417532) on vimeo.

## Questions and Issues

Please submit a GitHub Issue for any question or issue.

## Converting Crescendo programs to 2-Series

This document provides instructions for converting "The Loft" demo from a 3-Series (CP3N) to 2-Series processor (PRO2).

All Crescendo modules are 2-Series compatible. While it is advised systems take advantage of the additional features and processing power of 3-Series control systems, Crescendo will run reliably on 2-Series control systems.

Crescendo UIs make extensive use of the `Subpage Reference List` to deliver dynamic menus to the UI, and minimal use of all other Smart Graphics Objects. Smart Graphics interfaces are supported by 2-Series control systems. The `Media Player Application` used to control music servers, like the Crestron NSP-1, is not supported by 2-Series control systems.

### Instructions

1. Open `Program/Crescendo Loft.smw` and enter _Configure_ mode.
2. Right-Click and **replace** the CP3N with a PRO2
3. Click **Yes** to proceed and **Yes** to keep the changes.<br>_SIMPL Windows will attempt to add devices to retain current equipment and associated logic. The application will also remove any modules that are not 2-Series compatible._
4. Delete the **Media Player Application** Smart Graphics Extender from Touchscreens 01-05.<br>_The `Media Player Object Router v3.0` modules are removed from logic during the conversion._
5. Uncomment the `Make String Permanent` symbols for each touchscreen utilizing Smart Object Programming.<br>_Serial signals connected to Smart Graphics Extenders will not display in 2-Series without this additional `MSP`._
6. Compile the program. The compiler should report 0 errors, 0 warnings, and 0 notices.
