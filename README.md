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
| 8 | Climates | 8000     |
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
| 5 | Sources    | Source   | 80[ID]   |
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

| Inputs     | Outputs                           |
|:-----------|:----------------------------------|
|            | Room_01_Exists ... Room_99_Exists |


#### Room

| Inputs                  |  Outputs      |
|:------------------------|:--------------|
| **Self**                                |
|                         | Meta~         |
|                         | Name$         |
|                         | Description$  |
| **Common_Controls**                     |
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

| Room Parameters |
|:----------------|
| Name            |
| ID              |
| Audio Switchers |
| Video Switchers |
| Video Menu      |
| Audio Menu      |
| Sources         |
| Lights          |
| Shades          |
| Climate         |
| Default Source  |


#### Area

| Inputs                  |  Outputs      |
|:------------------------|:--------------|
| **Self**                                |
|                         | Meta~         |
|                         | Name$         |
|                         | Description$  |
| **Common_Controls**                     |
| Source_ID~              |               |
| Powered_By_Rooms        |               |
| Power_On/Off            |               |
| Power_On                | Power_On_Fb   |
| Power_Off               | Power_Off_Fb  |
| Volume~                 |               |
| Volume_Up               |               |
| Volume_Down             |               |
| Mute                    |               |
| Mute_On                 |               |
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

| Area Parameters |
|:----------------|
| Name            |
| ID              |
| Rooms           |
| Video Menu      |
| Audio Menu      |
| Lights          |
| Shades          |
| Climate         |
| Default Source  |


#### Switcher

| Inputs                  |  Outputs              |
|:------------------------|:----------------------|
| **Self**                                        |
|                         | Meta~                 |
|                         | Initialized!          |
| **Device**                                      |
| Source_Route~           | Source_ID             |
| Power_Fb                | Powered               |
| Power_On/Off            |                       |
|                         | Power_On/Off          |
| Set_Power_On            | Power_On              |
| Set_Power_Off           | Power_Off             |
| Volume_Is               | Volume~               |
| Volume_Control_Is       | Volume_Up             |
|                         | Volume_Down           |
| Mute_Fb                 | Muted                 |
|                         | Mute_On/Off           |
|                         | Mute_On               |
|                         | Mute_Off              |
| Input_Is                | Input                 |
|                         | Input~                |
|                         | Input_01 ... Input_16 |

| Switcher Parameters                           |
|:----------------------------------------------|
| Name                                          |
| ID                                            |
| Warm-up Time                                  |
| Volume Control                                |
| Input Changes                                 |
| Sources for Power Off                         |
| Sources for Input 01 ... Sources for Input 64 |


#### Source

| Inputs                                |  Outputs                      |
|:--------------------------------------|:------------------------------|
| **Self**                                                              |
|                                       | Meta~                         |
| Initialize                            | Initialized                   |
|                                       | Initialized!                  |
|                                       | Connected                     |
|                                       | Connected!                    |
|                                       | Disconnected!                 |
|                                       | Name$                         |
| Set_Status                            | Status$                       |
| Set_Color                             |                               |
| **Common_Controls**                                                   |
|                                       | Cursor_Up                     |
|                                       | Cursor_Down                   |
|                                       | Cursor_Left                   |
|                                       | Cursor_Right                  |
|                                       | Cursor_Select                 |
|                                       | Guide                         |
|                                       | Info                          |
|                                       | Menu                          |
|                                       | Exit                          |
| Playing                               | Play                          |
| Stopped                               | Stop                          |
| Paused                                | Pause                         |
| Scanning_Forward                      | Scan_Forward                  |
| Scanning_Back                         | Scan_Back                     |
|                                       | Skip_Forward                  |
|                                       | Skip_Back                     |
|                                       | Record                        |
|                                       | Page_Up                       |
|                                       | Page_Down                     |
|                                       | Number_0 ... Number_9         |
|                                       | Number_Enter                  |
|                                       | Number_Clear                  |
|                                       | Channel_Up                    |
|                                       | Channel_Down                  |
|                                       | Channel_Recall                |
|                                       | Return                        |
|                                       | Red                           |
|                                       | Green                         |
|                                       | Yellow                        |
|                                       | Blue                          |
|                                       | List                          |
|                                       | Live                          |
|                                       | Fav                           |
|                                       | F1 ... F10                    |
|                                       | Power_On                      |
|                                       | Power_Off                     |
| **Digitals**                          |                               |
| Digital_101_Fb ... Digital_298_Fb     | Digital_101 ... Digital_298   |
| **Analogs**                           |                               |
| Analog_101_Fb ... Analog_398_Fb       |                               |
| **Serials**                           |                               |
| Serial_101_Fb ... Serial_110_Fb       | Serial_101 ... Serial_110     |
| Serial_111_Fb ... Serial_398_Fb       |                               |


#### Sources

| Inputs                  |  Outputs                              |
|:------------------------|:--------------------------------------|
|                         | Source_01_Exists ... Source_99_Exists |


#### Touchscreen

| Inputs                                |  Outputs                                                      |
|:--------------------------------------|:--------------------------------------------------------------|
| **Self**                                                                                              |
| Route~                                | Initialized!                                                  |
| Generic_Route~                        |                                                               |
|                                       | Source_Has_Audio                                              |
|                                       | Source_Has_Video                                              |
| **Digitals**                          |                                                               |
| Power_On/Off                          |                                                               |
| Power_On                              | Power_On_Fb                                                   |
| Power_Off                             | Power_Off_Fb                                                  |
| Power_Subpage_Show                    | Power_Subpage_Showing                                         |
| Power_Subpage_Hide                    |                                                               |
| Sleep_Cancel                          |                                                               |
| Sleep_In_30_Set                       | Sleep_In_30_Active                                            |
| Sleep_In_60_Set                       | Sleep_In_60_Active                                            |
| Sleep_In_90_Set                       | Sleep_In_90_Active                                            |
| Sleep_In_120_Set                      | Sleep_In_120_Active                                           |
|                                       | Volume_Subpage_Showing                                        |
| Volume_Up                             |                                                               |
| Volume_Down                           |                                                               |
| Volume_Sliding                        |                                                               |
| Mute                                  | Mute_Fb                                                       |
| Mute_On                               | Volume_Control_Is_Absolute                                    |
| Mute_Off                              | Volume_Control_Is_Relative                                    |
|                                       | Volume_Control_Is_Area                                        |
| Control_Source                        |                                                               |
| Digital_101 ... Digital_298           | Digital_101_Fb ... Digital_298_Fb                             |
| Cursor_Up                             |                                                               |
| Cursor_Down                           |                                                               |
| Cursor_Left                           |                                                               |
| Cursor_Right                          |                                                               |
| Cursor_Select                         |                                                               |
| Guide                                 |                                                               |
| Info                                  |                                                               |
| Menu                                  |                                                               |
| Exit                                  |                                                               |
| Play                                  | Playing                                                       |
| Stop                                  | Stopped                                                       |
| Pause                                 | Paused                                                        |
| Scan_Forward                          | Scanning_Forward                                              |
| Scan_Back                             | Scanning_Back                                                 |
| Skip_Forward                          |                                                               |
| Skip_Back                             |                                                               |
| Record                                | Recording                                                     |
| Page_Up                               |                                                               |
| Page_Down                             |                                                               |
| Number_0 ... Number_9                 |                                                               |
| Number_Enter                          |                                                               |
| Number_Clear                          |                                                               |
| Channel_Up                            |                                                               |
| Channel_Down                          |                                                               |
| Channel_Recall                        |                                                               |
| Back                                  |                                                               |
| Red                                   |                                                               |
| Green                                 |                                                               |
| Yellow                                |                                                               |
| Blue                                  |                                                               |
| List                                  |                                                               |
| Live                                  |                                                               |
| Format                                |                                                               |
| Menu_A_Item_01 ... Menu_A_Item_48     | Menu_A_Item_01_Highlighted ... Menu_A_Item_48_Highlighted     |
| Menu_A_Back                           | Menu_A_Back_Showing                                           |
| Menu_A_Page_Up                        | Menu_A_Page_Up_Showing                                        |
| Menu_A_Page_Down                      | Menu_A_Page_Down_Showing                                      |
|                                       | Menu_A_Page_01_Focused ... Menu_A_Page_16_Focused             |
| Menu_B_Item_01 ... Menu_B_Item_48     | Menu_B_Item_01_Highlighted ... Menu_B_Item_48_Highlighted     |
| Menu_B_Back                           | Menu_B_Back_Showing                                           |
| Menu_B_Page_Up                        | Menu_B_Page_Up_Showing                                        |
| Menu_B_Page_Down                      | Menu_B_Page_Down_Showing                                      |
|                                       | Menu_B_Page_01_Focused ... Menu_B_Page_16_Focused             |
| Menu_C_Item_01 ... Menu_B_Item_48     | Menu_C_Item_01_Highlighted ... Menu_C_Item_48_Highlighted     |
| Menu_C_Back                           | Menu_C_Back_Showing                                           |
| Menu_C_Page_Up                        | Menu_C_Page_Up_Showing                                        |
| Menu_C_Page_Down                      | Menu_C_Page_Down_Showing                                      |
|                                       | Menu_C_Page_01_Focused ... Menu_C_Page_16_Focused             |
| Page_Clear                            |                                                               |
| Page_Home                             | Page_01_Showing                                               |
|                                       | Page_02_Showing ... Page_88_Showing                           |
| Subpage_1 ... Subpage_6               | Subpage_1_Showing ... Subpage_6_Showing                       |
| **Analogs**                           |                                                               |
|                                       | Room_Route                                                    |
|                                       | Source_Route                                                  |
|                                       | Room_Icon                                                     |
| Volume                                | Volume_Fb                                                     |
|                                       | Mute_Mode                                                     |
| Analog_101 ... Analog_110             | Analog_101_Fb ... Analog_110_Fb                               |
|                                       | Analog_111_Fb ... Analog_298_Fb                               |
|                                       | Menu_A_Item_01_Icon ... Menu_A_Item_48_Icon                   |
|                                       | Menu_A_Item_01_Color ... Menu_A_Item_48_Color                 |
|                                       | Menu_B_Item_01_Icon ... Menu_B_Item_48_Icon                   |
|                                       | Menu_B_Item_01_Color ... Menu_B_Item_48_Color                 |
|                                       | Menu_C_Item_01_Icon ... Menu_C_Item_48_Icon                   |
|                                       | Menu_C_Item_01_Color ... Menu_C_Item_48_Color                 |
|                                       | Menu_A_Item_Count                                             |
|                                       | Menu_A_Highlight                                              |
|                                       | Menu_B_Item_Count                                             |
|                                       | Menu_B_Highlight                                              |
|                                       | Menu_C_Item_Count                                             |
|                                       | Menu_C_Highlight                                              |
| **Serials**                           | Room_Name$                                                    |
|                                       | Source_Name$                                                  |
|                                       | Generic_Name$                                                 |
|                                       | Sleep_Message                                                 |
|                                       | Volume$                                                       |
|                                       | Serial_101_Fb ... Serial_298_Fb                               |
|                                       | Menu_A_Title                                                  |
|                                       | Menu_A_Item_01_Title ... Menu_A_Item_48_Title                 |
|                                       | Menu_A_Item_01_Description ... Menu_A_Item_48_Description     |
|                                       | Menu_A_Description                                            |
|                                       | Menu_B_Title                                                  |
|                                       | Menu_B_Item_01_Title ... Menu_A_Item_48_Title                 |
|                                       | Menu_B_Item_01_Description ... Menu_A_Item_48_Description     |
|                                       | Menu_B_Description                                            |
|                                       | Menu_C_Title                                                  |
|                                       | Menu_C_Item_01_Title ... Menu_A_Item_48_Title                 |
|                                       | Menu_C_Item_01_Description ... Menu_A_Item_48_Description     |
|                                       | Menu_C_Description                                            |

| Touchscreen Parameters        |
|-------------------------------|
| Name                          |
| ID                            |
| Default Room                  |
| Default Menu A                |
| Default Menu B                |
| Default Menu C                |
| Rooms                         |

