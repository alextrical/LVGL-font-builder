# LVGL Font Builder Action

This GitHub Action automates the generation of optimized C-source font files for the [LVGL (Light and Versatile Graphics Library)](https://lvgl.io/) ecosystem. 

## Overview
Manually managing font conversion for embedded UI projects can be tedious. This workflow streamlines the process by:
- Downloading the latest Montserrat TrueType font.
- Using `lv_font_conv` to convert fonts into C arrays.
- Applying specific ranges and sizes (12, 16, 20, 30) for memory-efficient UI development.
- Artifacting the generated `.c` files for immediate use in your firmware builds.

## Workflow Usage
To use this in your own repository, copy the workflow YAML into your `.github/workflows/` directory.

### Configuration
The workflow triggers on `workflow_dispatch` (manual) or whenever the workflow file itself is updated. You can customize the `RANGE` variable in the script to support specific character sets (e.g., Extended Latin or Symbols) required by your application.

## Credits
- Built using [lv_font_conv](https://github.com/lvgl/lv_font_conv).
- Montserrat font provided by [Julieta Ula](https://github.com/JulietaUla/Montserrat).
