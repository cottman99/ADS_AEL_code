# ADS Custom Layout Functions

[中文文档](README_CN.md)

## Description
A collection of Advanced Design System (ADS) layout functions written in AEL (Application Extension Language) for automated generation of various inductor structures. This toolkit provides functions to draw complex inductor layouts including multi-turn octagonal inductors, intersection structures, and terminals.

## Features
- Multi-ring inductor generation with customizable parameters
- Octagonal inductor layout with configurable dimensions
- Support for both single-ring and multi-turn inductor structures
- Automated intersection handling for multi-layer designs
- Customizable terminal configurations
- Hollow rectangle and specialized octagon drawing functions
- Flexible layer management (wire layer, under layer, via layer)
- Parametric control for:
  - Number of turns
  - Spacing between turns
  - Path width
  - Corner coefficients
  - Terminal dimensions

## Installation
```AEl
1. Copy all .ael files to your ADS workspace
2. Load the required functions in ADS using:
   load("include.ael");
   # Or load individual functions as needed
```

## Usage
```scheme
# Example: Drawing a multi-ring inductor
draw_inductor_multi_ring(
    centerX,            # Center X coordinate
    centerY,            # Center Y coordinate
    Nturns,            # Number of turns
    spacing,           # Spacing between turns
    lengthX,           # X direction length
    lengthY,           # Y direction length
    cornerK,           # Corner coefficient
    pathWidth,         # Wire width
    wireLayerName,     # Wire layer name
    underLayerName,    # Under layer name
    viaLayerName,      # Via layer name
    terminalmode,      # Terminal mode
    terminalWidth,     # Terminal width
    terminalLength,    # Terminal length
    terminalGap,       # Terminal gap
    intersection_spacing_ratio  # Intersection spacing ratio
);
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author
- Author: PhiChi
- Zhihu: [PATactics](https://www.zhihu.com/people/flyzi-you-58)

## Acknowledgments
Special thanks to Keysight Technologies for developing the excellent Advanced Design System (ADS) software. 