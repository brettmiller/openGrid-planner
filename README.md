# OpenGrid Planner

A web-based planning tool for designing OpenGrid layouts with precision. Optimized for BambuLab 3D printers and compatible with the Gridfinity ecosystem (28mm grid system).

*Initially inspired by and built upon [this Claude artifact](https://claude.ai/public/artifacts/6e5392ba-b387-4203-a8f1-577336c0b0b8), significantly expanded with additional features and optimization modes.*

## Features

- **Two Layout Modes**
  - **Auto Optimal Mode**: Analyzes your dimensions and recommends the top 10 tile configurations sorted by coverage efficiency
  - **Manual Size Mode**: Specify exact tile dimensions for custom layouts

- **Optimization Strategies**
  - **Single tile size**: All tiles identical - simpler to print, moderate coverage
  - **Multiple sizes (fill space)**: Uses edge and corner tiles for maximum coverage

- **BambuLab Printer Presets**
  - A1 Mini (180×180×180mm)
  - A1 (256×256×256mm)
  - P1P, P1S, X1 Carbon (256×256×256mm)
  - Custom bed size option

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

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/brettmiller/opengrid-planner.git
cd opengrid-planner
```

2. Start a local web server:
```bash
python3 -m http.server 8080
```

3. Open your browser to:
```
http://localhost:8080/opengrid-planner.html
```

### Quick Start

1. **Enter Wall Dimensions**: Input width and height in mm or inches
2. **Select Your Printer**: Choose your BambuLab printer model
3. **Choose Layout Mode**: 
   - Use Auto Optimal to see top recommendations
   - Use Manual Size for specific tile dimensions
4. **Select Tile Type**: Regular or Lite
5. **Calculate**: Click "Calculate Layout" to generate results
6. **Review**: Check the visual preview and parts list

## Tips for Full Bed Usage

When printing tiles that use the full bed size (9×9 grids or similar):

- **Disable Skirt/Brim**: Allows for larger parts on the plate
- **Calibrations**: May need to disable auto-flow calibration for extra room
- **Check Z-Hop**: Ensure Z-hop setting doesn't exceed 256mm height limit

## OpenGrid Specifications

- **Grid Size**: 28mm (Gridfinity compatible)
- **Regular Tiles**: 3m4s per grid square
- **Lite Tiles**: 1m38s per grid square
- **Connection System**: Multiconnect connectors

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
