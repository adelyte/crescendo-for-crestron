# Crescendo Framework

Crescendo is a free (both _gratis_ and _libre_) software framework for Crestron control systems designed by [Adelyte Company](https://www.adelyte.com/). Please visit the [project page](https://www.adelyte.com/crestron/crescendo) and [documentation](https://www.adelyte.com/crestron/crescendo/docs) for more information.

## Best Practices
### General

  1. Modular design.
  2. Model–view–controller architecture.

### Crestron-Specific

  1. Organized and optimized for SIMPL Debugger.
  2. Compatible with 2-Series and 3-Series processors.
  3. Minimal use of SIMPL+.
  4. Fast compile time.
  5. Low memory utilization and very fast execution.

## Standards and Style
### Crosspoint Routing
#### Equipment Routes

| # | Model    | Route    |
|:--|:---------|---------:|
| 1 | Rooms    | 1000     |
| 1 | Room     | 10[ID]   |
| 2 | Audio    | 20[ID]   |
| 3 | Video    | 30[ID]   |
| 4 | Switcher | 40[ID]   |
| 5 | Sources  | 5000     |
| 5 | Source   | 50[ID]   |
| 6 | Lighting | 60[ID]   |
| 7 | Shades   | 70[ID]   |
| 8 | Climate  | 80[ID]   |
| 9 | Generic  | 90[ID]   |
| A | Menu A   | A0[ID]   |
| B | Menu B   | B0[ID]   |
| C | Menu C   | C0[ID]   |

#### Control Routes

| # | Model      | Target   | Route    |
|:--|:-----------|:---------|---------:|
| 1 | Rooms      | Room     | 10[ID]   |
| 1 | Area       | Room     | 11[ID]   |
| 1 | Room       | Audio    | 12[ID]   |
| 1 | Room       | Video    | 13[ID]   |
| 1 | Room       | Source   | 15[ID]   |
| 4 | Switcher   | Source   | 45[ID]   |
| 5 | Sources    | Source   | 50[ID]   |
| A | Touchpanel | Rooms    | A0[ID]   |
| A | Touchpanel | Room     | A1[ID]   |
| A | Touchpanel | Generic  | A9[ID]   |
| A | Touchpanel | Menu A   | AA[ID]   |
| A | Touchpanel | Menu B   | AB[ID]   |
| A | Touchpanel | Menu C   | AC[ID]   |
| B | Remote     | Room     | B1[ID]   |
| B | Remote     | Generic  | B9[ID]   |

### Modules
#### Rooms

| Outputs                                           |
|:--------------------------------------------------|
| //R-xx__Room_01_Exists ... //R-xx__Room_99_Exists |

#### Room
##### Room 01
| Inputs                  |  Outputs      |
|:------------------------|:--------------|
|                       Self              |
+-------------------------+---------------+
|                         | Meta~         |
|                         | Name$         |
|                         | Description$  |
| Common_Controls                         |
| Source_ID~              | Source_ID_Fb  |
| Power_On/Off            |               |
| Power_On                | Power_On_Fb   |
| Power_Off               | Power_Off_Fb  |
| Volume~                 | Volume_Fb     |
| Volume_Up               |               |
| Volume_Down             |               |
| Mute                    |               |
| Mute_On                 | Mute_Fb       |
| Mute_Off                |               |
| Play                    |               |
| Stop                    |               |
| Pause                   |               |
| Scan_Forward            |               |
| Scan_Back               |               |
| Skip_Forward            |               |
| Skip_Back               |               |
| Channel_Up              |               |
| Channel_Down            |               |
| Preset_01 ... Preset_10 |               | 




|       |       |       |
|:------|:------|:------|
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |


|       |       |       |
|:------|:------|:------|
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |


|       |       |       |
|:------|:------|:------|
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |
|       |       |       |

|Common Controls                                    |



|Parameters  table |

