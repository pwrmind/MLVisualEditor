# Brain.js Visual Editor

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Brain.js](https://img.shields.io/badge/brain.js-2.0.0--beta.1-orange)](https://brain.js.org)
[![Alpine.js](https://img.shields.io/badge/alpine.js-3.13.0-77c1d2)](https://alpinejs.dev)
[![Bootstrap](https://img.shields.io/badge/bootstrap-5.3.0-7952b3)](https://getbootstrap.com)

A modern, browser-based visual editor for creating, training, and visualizing neural networks using Brain.js. This single-page application provides an intuitive interface for machine learning without writing code.

![Brain.js Visual Editor Screenshot](https://via.placeholder.com/800x450/4361ee/ffffff?text=Brain.js+Visual+Editor)

## Features

- 🎨 **Visual Network Builder** - Drag-and-drop interface for designing neural network architectures
- 🤖 **Multiple Network Types** - Support for NeuralNetwork, LSTM, GRU, LSTMTimeStep, and Autoencoder
- 📊 **Real-time Visualization** - Interactive D3.js visualizations of network structure and training progress
- 📈 **Training Monitor** - Live charts showing error reduction during training
- 💾 **Model Management** - Save, load, and export trained models
- 🎯 **Built-in Datasets** - Preloaded XOR demo data for quick testing
- 📱 **Responsive Design** - Works on desktop and tablet devices
- 🚀 **No Installation Required** - Runs entirely in the browser

## Live Demo

Try the editor directly in your browser: [Live Demo](https://pwrmind.github.io/MLVisualEditor/)

## Quick Start

### Option 1: Direct Usage
1. Download `index.html` from this repository
2. Open it in any modern web browser (Chrome, Firefox, Safari, Edge)
3. Start building neural networks immediately!

### Option 2: Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/brainjs-visual-editor.git

# Navigate to the project directory
cd brainjs-visual-editor

# Open index.html in your browser
# No build process required - it's a single HTML file!
```

## How to Use

### 1. Design Your Network
1. Select network type from the dropdown (NeuralNetwork, LSTM, etc.)
2. Configure input and output sizes
3. Add and configure hidden layers
4. Choose activation functions (sigmoid, ReLU, tanh, etc.)

### 2. Prepare Your Data
- Use the built-in XOR dataset for testing
- Import your own JSON training data
- Create custom examples with random data
- Export datasets for reuse

### 3. Train Your Model
1. Set training parameters (iterations, error threshold, learning rate)
2. Click "Start Training" to begin
3. Monitor progress with real-time error charts
4. Stop training anytime

### 4. Test & Export
- Test the trained model with custom inputs
- Use forecasting for time series networks
- Save models to browser storage
- Export models as JSON for use in other projects

## Supported Network Types

| Network Type | Best For | Features |
|--------------|----------|----------|
| NeuralNetwork | Classification, Regression | Feedforward, Backpropagation |
| LSTM | Time Series, Sequence Prediction | Long-term memory, Time steps |
| GRU | Text Generation, Sequence Modeling | Gated recurrent units |
| LSTMTimeStep | Forecasting, Pattern Recognition | Time series forecasting |
| AE (Autoencoder) | Dimensionality Reduction, Anomaly Detection | Encoder-decoder architecture |

## API Reference

### Training Data Format
```javascript
// For NeuralNetwork
const data = [
  { input: [0, 0], output: [0] },
  { input: [0, 1], output: [1] },
  { input: [1, 0], output: [1] },
  { input: [1, 1], output: [0] }
];

// For RNN/LSTM (strings)
const textData = [
  { input: "hello", output: "world" },
  { input: "machine", output: "learning" }
];

// For Time Series
const timeSeriesData = [
  [1, 2, 3, 4, 5],
  [2, 3, 4, 5, 6]
];
```

### Model Configuration
```javascript
const config = {
  inputSize: 2,
  hiddenLayers: [3, 4],  // Two hidden layers
  outputSize: 1,
  activation: 'sigmoid',
  learningRate: 0.3,
  binaryThresh: 0.5
};
```

## Examples

### XOR Problem
The classic XOR problem is included as a demo. Watch the network learn to solve this non-linear problem in real-time.

### Time Series Forecasting
Use LSTMTimeStep to predict future values from sequential data. Perfect for stock prices, weather data, or any temporal patterns.

### Text Generation
Experiment with LSTM networks to generate text based on training patterns.

## Technology Stack

- **Brain.js** - GPU-accelerated neural networks in JavaScript
- **Alpine.js** - Minimal framework for reactive JavaScript
- **Bootstrap 5** - Responsive CSS framework
- **D3.js** - Data visualization library
- **Font Awesome** - Icon toolkit
- **Google Fonts** - Typography

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Limitations

- Maximum training data size limited by browser memory
- Training may be slower than native implementations
- GPU acceleration depends on WebGL support
- No server-side processing (all computation happens in browser)

## Troubleshooting

### Common Issues

1. **"Brain is not defined" error**
   - Ensure you have internet connection to load Brain.js CDN
   - Check browser console for network errors

2. **Slow training performance**
   - Reduce network size or training iterations
   - Close other browser tabs to free memory

3. **Visualization not updating**
   - Refresh the page
   - Check if D3.js loaded properly

4. **Model saving issues**
   - Ensure localStorage is enabled in your browser
   - Clear browser cache if problems persist

## Contributing

We welcome contributions! Here's how you can help:

1. **Report Bugs** - Open an issue with detailed description
2. **Suggest Features** - Share your ideas for improvement
3. **Submit Pull Requests** - Fix bugs or add new features
4. **Improve Documentation** - Help make the project more accessible

### Development Setup
```bash
# No build system required - just edit index.html!
```

### Project Structure
```
brainjs-visual-editor/
├── index.html          # Complete application (single file)
├── README.md           # This file
└── assets/             # (Future) Additional resources
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Brain.js Team](https://github.com/BrainJS) - For the amazing neural network library
- [Alpine.js](https://alpinejs.dev) - For the lightweight reactivity
- [D3.js](https://d3js.org) - For powerful visualization capabilities
- All contributors and users of this project

## Related Projects

- [Brain.js](https://github.com/BrainJS/brain.js) - Core neural network library
- [TensorFlow.js](https://www.tensorflow.org/js) - Google's ML library for JavaScript
- [ml5.js](https://ml5js.org) - Friendly machine learning for the web

## Support

If you find this project useful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting issues
- 💡 Suggesting features
- 🔄 Sharing with others

---

Built with ❤️ by the open-source community. Happy neural networking! 🧠✨
