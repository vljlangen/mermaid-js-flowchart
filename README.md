# FlowchartWizard JS + Mermaid

A simple web application for creating uniform-sized flowcharts using Mermaid.js with automatic text padding to ensure consistent node dimensions.

## Features

- **Uniform Node Sizing**: Automatically pads text to make all flowchart nodes the same width
- **Multi-line Support**: Use line breaks within nodes for multi-line text
- **Title Support**: Option to use the first line as a chart title
- **Real-time Rendering**: Instant flowchart generation as you type
- **Clean UI**: Simple, intuitive interface for flowchart creation

## How It Works

The application uses a clever workaround to ensure all nodes are the same size:

1. **Text Analysis**: Scans all node text to find the longest line
2. **Padding Algorithm**: Adds padding spaces (or 'X' characters for debugging) to shorter lines
3. **Even Distribution**: Distributes padding evenly on both sides of the text
4. **Mermaid Rendering**: Generates a Mermaid flowchart with uniformly sized nodes

## Usage

1. Open `index.html` in your web browser
2. Enter your flowchart steps in the textarea:
   - Use empty lines to separate different nodes
   - Use line breaks (Enter) within a node for multi-line text
3. Check "Use first line as chart title" if you want the first line to be a title
4. Click "Draw Flowchart" to generate your chart

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
- **Padding Method**: Character-based padding with even distribution
- **Debug Mode**: Uses 'X' characters for visual padding debugging

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

## License

MIT License - see LICENSE file for details.

## Contributing

Feel free to submit issues and enhancement requests!
