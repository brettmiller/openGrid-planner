# OpenGrid Planner

A web-based planning tool for designing OpenGrid layouts with precision. With defaults for BambuLab 3D printers.

*Initially inspired by and built upon [this Claude artifact](https://claude.ai/public/artifacts/6e5392ba-b387-4203-a8f1-577336c0b0b8), significantly expanded with additional features and optimization modes.*

###### This was entirely created with Claude, primarly Sonnet 4.5

## Features

- **Two Layout Modes**
  - **Auto Optimal Mode**: Analyzes your dimensions and recommends the top 10 tile configurations sorted by coverage efficiency
  - **Manual Size Mode**: Specify exact tile dimensions for custom layouts

- **Optimization Strategies**
  - **Single tile size**: All tiles identical - simpler to print, moderate coverage
  - **Multiple sizes (fill space)**: Uses different size edge and corner tiles for maximum coverage
  - **Multiple sizes (in manual size layout mode)**: has additional option to prefer enlarging edge row/column tiles to fit over uing smaller edge tiles 

- **BambuLab Printer Presets**
  - A1 Mini (180×180×180mm)
  - A1 (256×256×256mm)
  - P1P, P1S, X1 Carbon (256×256×256mm)
  - Custom bed size option (length and width can be specified in mm)

- **Dual Unit Support**
  - mm and inch measurements
  - Built-in unit converter with fraction support (e.g., 3 5/16")
  - Auto-conversion when switching units

- **Tile Types**
  - **Regular**: Stronger construction, 3m4s per grid square
  - **Lite**: Faster printing, 1m38s per grid square

- **Visual Preview**
  - See exactly how tiles fit on your wall
  - Color-coded tile types (main, edge, corner)
  - Coverage percentage and unused space visualization

- **Complete Parts List**
  - Detailed breakdown of all tile sizes needed
  - Multiconnect connector count
  - Estimated total print time

## Usage

1. **Enter Wall Dimensions**: Input width and height in mm or inches
1. **Select Your Printer**: Choose your BambuLab printer model
1. **Choose Layout Mode**:
   - Use Auto Optimal to see top recommendations
   - Use Manual Size for specific tile dimensions
1. **Select Tile Type**: Regular or Lite
1. **Calculate**: Click "Calculate Layout" to generate results
1. **Review**: Check the visual preview and parts list

## Tips for Full Bed Usage

When printing tiles that use the full bed size (9×9 grids or similar):

- **Disable Skirt/Brim**: Allows for larger parts on the plate
- **Calibrations**: May need to disable auto-flow calibration for extra room
- **Check Z-Hop**: Ensure Z-hop setting doesn't exceed 256mm height limit

## Technical Details

- Pure HTML/CSS/JavaScript - no build step required
- Responsive design for desktop and mobile
- No external dependencies
- Single file application for easy deployment

## Browser Compatibility

Works in all modern browsers:

- Chrome/Edge (recommended)
- Firefox
- Safari

## License

MIT License - feel free to use, modify, and distribute.

## Credits

Created for the OpenGrid and Gridfinity communities. Compatible with the 28mm grid standard.

## Contributing

Issues and pull requests welcome! Please ensure changes maintain the single-file architecture for ease of deployment.
