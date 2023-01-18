# Adding Themes

***SHORT ANSWER:*** if you're just looking to change the accent color for one of the already available palettes, then just change the keys marked as 'Accent' in the table below. This should yeald you a solid starting point with just occasional / minor imperfections.\
*If you succeed, feel free to submit a Pull Request to get this project closer to completion!*

---

***LONG ANSWER (walkthrough):***\
Theming in Cura is done (sadly) through a JSON file. Each key is then  called at startup in QML to load the UI colors (reason why there is no live reloading).\
This means that it's often not very easy to find correct keys or figure out exactly which ones do what.

Here is an example of a JSON string:

```json
"background_1": [30, 30, 46, 255]
```

... which in practice means:

```yaml
"UI Element": [Red, Green, Blue, Alpha]
```

A table to convert and explain JSON keys is provided below. Any contributions and corrections are welcome.

## Conversion notes

|       **JSON Key** | **Colours**    |      **The color of...**       |
| -----------------: | :------------- | :----------------------------: |
|     `background_1` | Base           |                                |
|     `background_2` | Surface 0      |                                |
|     `background_3` | Surface 1      |                                |
|     `background_4` | Crust          |                                |
|         `accent_1` | Accent         |                                |
|         `accent_2` | Accent         |                                |
|      `border_main` | Crust          |   thin lines b/w UI elements   |
|  `border_accent_1` | Accent         |                                |
|  `border_accent_2` | Accent         |                                |
|     `border_field` | ***?????***    |        unknown / unused        |
|     `text_default` | Text           |        most of the text        |
|    `text_disabled` | Overlay 1      |       unselectable text        |
|  `text_link_hover` | ***?????***    |        unknown / unused        |
|     `text_lighter` | Overlay 1      | stuff like shortcut indicators |
|      ---section--- | ---section---  |         ---section---          |
|           `lining` | `border_main`  |    basically `border_main`     |
|      `wide_lining` | ***?????***    |        unknown / unused        |
|     `thick_lining` | ***?????***    |        unknown / unused        |
| `viewport_overlay` | `background_1` |   color of the *MONITOR* tab   |
|                    |                |                                |
