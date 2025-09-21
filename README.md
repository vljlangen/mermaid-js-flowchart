# Funky Flowcharts

**World's Fastest, Funkiest, Free-est Flowchart-o-matic** - A simple web application for creating beautiful, uniform-sized flowcharts using Mermaid.js with automatic text padding to ensure consistent node dimensions.

## Features

- **Uniform Node Sizing**: Automatically pads text with invisible characters to make all flowchart nodes the same width
- **Multi-line Support**: Use line breaks within nodes for multi-line text
- **Real-time Rendering**: Instant flowchart generation as you type
- **Multiple Export Formats**: Export as SVG, PNG, or PDF
- **Print Support**: Clean printing with interface elements hidden
- **Invisible-X Padding**: Uses clever invisible character padding for perfect node alignment
- **Clean UI**: Simple, intuitive interface for flowchart creation

## How It Works

The application uses a clever "Invisible-X Padding" technique to ensure all nodes are the same size:

1. **Text Analysis**: Scans all node text to find the longest line across all nodes
2. **Invisible Padding**: Adds invisible `<span style="visibility:hidden">X</span>` characters to shorter lines
3. **Even Distribution**: Distributes padding evenly on both sides of the text
4. **Mermaid Rendering**: Generates a Mermaid flowchart with uniformly sized nodes
5. **Export Processing**: Cleans up invisible characters during export for clean output

## Usage

1. Open `index.html` in your web browser
2. Enter your flowchart steps in the textarea:
   - Use empty lines to separate different nodes
   - Use line breaks (Enter) within a node for multi-line text
3. Click "Draw Flowchart" to generate your chart
4. Export your flowchart:
   - **SVG**: For vector graphics and further editing
   - **PNG**: For high-resolution images
   - **PDF**: For documents and presentations
   - **Print**: Clean printing with interface hidden

### Example Input

```
The Health 2000 study participants
aged ≥ 30 yrs with a TSH result
(N=XXXX)

Thyroid-healthy population
(n=XXXX)

Risk factor-free population
(n=XXXX)

Reference population
(n=XXXX)
```

## Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (ES6 modules)
- **Chart Engine**: Mermaid.js v10
- **Padding Method**: Invisible character padding with even distribution
- **Export Libraries**: PDFKit + SVG-to-PDFKit for PDF generation
- **Arrow Handling**: Custom arrow marker conversion for PDF compatibility
- **Text Centering**: Automatic text centering within nodes

## File Structure

```
flowchart/
├── index.html          # Main application file
├── .gitignore         # Git ignore rules
├── README.md          # This file
└── LICENSE            # MIT License
```

## Browser Compatibility

- Modern browsers with ES6 module support
- Chrome 61+
- Firefox 60+
- Safari 10.1+
- Edge 16+

## Development

This is a client-side only application. Simply open `index.html` in a web browser - no build process or server required.

## Advanced Usage

### Creating Two-Column Flowcharts

This automator creates only one-column vertical flowcharts. To create inclusion/exclusion flowcharts with two columns:

1. Create two separate one-column flowcharts
2. Export both as SVG
3. Arrange them side by side in vector software like Inkscape (free)
4. **Important**: Ungroup the objects many times in Inkscape to get granular control

### Export Tips

- **SVG Export**: Best for further editing and vector graphics
- **PNG Export**: High-resolution raster images (5x scaling for crisp output)
- **PDF Export**: Includes custom arrow handling for proper arrowhead display
- **Print**: Clean output with all interface elements hidden

## License

CC BY-SA 4.0 - Creative Commons Attribution-ShareAlike 4.0 International License

This web app uses Mermaid.js (MIT) under the hood for flowchart rendering.

## Contributing

Feel free to submit issues and enhancement requests! This project is open source and welcomes contributions.

## Author

Ville Langén, 2025
