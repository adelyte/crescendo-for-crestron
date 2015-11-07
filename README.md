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
| 6 | Lights   | 6000     |
| 6 | Light    | 60[ID]   |
| 7 | Shades   | 7000     |
| 7 | Shade    | 70[ID]   |
| 8 | Climates | 8000     |
| 8 | Climate  | 80[ID]   |
| 9 | Generic  | 90[ID]   |

#### Control Routes

| # | Control     | Target   | Route    |
|:--|:----------- |:---------|---------:|
| 1 | Rooms       | Room     | 10[ID]   |
| 1 | Area        | Room     | 11[ID]   |
| 1 | Room        | Audio    | 12[ID]   |
| 1 | Room        | Video    | 13[ID]   |
| 1 | Room        | Source   | 15[ID]   |
| 4 | Switcher    | Source   | 45[ID]   |
| 5 | Sources     | Source   | 50[ID]   |
| 6 | Lights      | Light    | 60[ID]   |
| 7 | Shades      | Shade    | 70[ID]   |
| 8 | Climates    | Climate  | 80[ID]   |
| 9 | Touchpanel  | Room     | 91[ID]   |
| 9 | Touchpanel  | Source   | 95[ID]   |
| 9 | Touchpanel  | Device   | 99[ID]   |
| A | Controller  | Rooms    | A1[ID]   |
| A | Controller  | Sources  | A5[ID]   |
| A | Controller  | Lights   | A6[ID]   |
| A | Controller  | Shades   | A7[ID]   |
| A | Controller  | Climates | A8[ID]   |
| B | Remote      | Room     | B1[ID]   |
| B | Remote      | Generic  | B9[ID]   |