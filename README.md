#  Hand Digit Recognition CNN

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10.13-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/TensorFlow-2.15.0-orange.svg" alt="TensorFlow Version">
  <img src="https://img.shields.io/badge/Streamlit-1.35.0-red.svg" alt="Streamlit Version">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</div>

<div align="center">
  <h3> A powerful CNN-based web application for real-time handwritten digit recognition</h3>
  <p>Draw digits (0-9) on an interactive canvas and get instant predictions powered by deep learning!</p>
</div>

---

##  Features

- ** Interactive Drawing Canvas** - Draw digits directly in your browser
- ** Real-time Predictions** - Instant digit recognition as you draw
- ** Deep Learning Powered** - Custom CNN architecture trained on MNIST dataset
- ** Responsive Design** - Works seamlessly on desktop and mobile devices
- ** Fast Processing** - Optimized model for quick inference
- ** High Accuracy** - Achieved excellent performance on test dataset

##  Architecture

### Model Structure
```
Conv2D(32, 3×3) → ReLU → MaxPool2D(2×2)
    ↓
Conv2D(32, 3×3) → ReLU → MaxPool2D(2×2)
    ↓
Flatten → Dense(128) → Sigmoid → Dense(10) → Softmax
```

### Key Specifications
- **Input Shape**: 28×28×1 (grayscale images)
- **Output**: 10 classes (digits 0-9)
- **Optimizer**: Adam
- **Loss Function**: Sparse Categorical Crossentropy
- **Training Dataset**: MNIST (60,000 training samples)

##  Quick Start

### Prerequisites
- Python 3.10.13
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Rakesh-ai-ds/hand_digit_recognition_cnn.git
   cd hand_digit_recognition_cnn
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run app.py
   ```

4. **Open your browser** and navigate to `http://localhost:8501`

##  Project Structure

```
hand_digit_recognition_cnn/
├── 📄 app.py                 # Streamlit web application
├── 📄 main.py                # Model training script
├── 📄 final.h5               # Pre-trained model weights
├── 📄 requirements.txt       # Python dependencies
├── 📄 runtime.txt           # Python version specification
└── 📄 README.md             # Project documentation
```

## 🎮 Usage

### Training Your Own Model
```bash
python main.py
```

This will:
- Load and preprocess the MNIST dataset
- Train the CNN model for 10 epochs
- Evaluate model performance
- Generate confusion matrix visualization
- Save the trained model as `final.h5`

### Running the Web App
```bash
streamlit run app.py
```

### Using the Interface
1. **Draw** a digit (0-9) on the black canvas using your mouse or touch
2. **Click** the "Predict" button
3. **View** the predicted digit result instantly

## 🔧 Technical Details

### Data Preprocessing
- Normalization: Pixel values scaled to [0, 1]
- Reshape: Images resized to 28×28 pixels
- Grayscale conversion for consistency

### Model Performance
- **Training Accuracy**: High accuracy achieved on MNIST dataset
- **Test Evaluation**: Comprehensive evaluation with confusion matrix
- **Real-time Inference**: Optimized for quick predictions

### Canvas Processing
- **Input**: 280×280 pixel drawing canvas
- **Processing**: Automatic resize to 28×28 for model input
- **Color**: Black background with white stroke for optimal recognition

##  Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| streamlit | 1.35.0 | Web application framework |
| streamlit-drawable-canvas | 0.9.3 | Interactive drawing component |
| tensorflow-cpu | 2.15.0 | Deep learning framework |
| numpy | 1.24.3 | Numerical computations |
| pillow | 10.2.0 | Image processing |
| matplotlib | 3.8.4 | Data visualization |
| seaborn | 0.13.2 | Statistical plotting |

##  Deployment

### Local Development
```bash
streamlit run app.py
```

### Production Deployment
The project includes configuration files for easy deployment:
- `runtime.txt` - Specifies Python version
- `requirements.txt` - Lists all dependencies

Compatible with platforms like:
- **Streamlit Cloud**
- **Heroku**
- **Google Cloud Platform**
- **AWS**

##  Contributing

We welcome contributions! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Areas for Improvement
- [ ] Add data augmentation for better generalization
- [ ] Implement model ensembling
- [ ] Add confidence scores display
- [ ] Create batch prediction functionality
- [ ] Add model performance metrics dashboard

##  Future Enhancements

- **Multi-language Support** - Support for different number systems
- **Advanced Preprocessing** - Enhanced image processing techniques
- **Model Optimization** - Quantization and pruning for faster inference
- **API Integration** - REST API for external applications
- **Mobile App** - Native mobile application

##  Troubleshooting

### Common Issues

**Issue**: Model loading error
```bash
# Solution: Ensure final.h5 exists in the project directory
python main.py  # This will create the model file
```

**Issue**: Canvas not responding
```bash
# Solution: Clear browser cache and refresh
Ctrl + F5 (Windows) or Cmd + R (Mac)
```

**Issue**: Poor prediction accuracy
```bash
# Solution: Draw digits clearly with proper contrast
- Use bold strokes
- Center the digit
- Ensure good contrast
```

##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

- **MNIST Dataset** - The foundation of handwritten digit recognition
- **TensorFlow Team** - For the amazing deep learning framework
- **Streamlit Community** - For the intuitive web app framework
- **Open Source Community** - For the tools and libraries that made this possible

---

<div align="center">
  <p>Made with ❤ by <a href="https://github.com/Rakesh-ai-ds">Rakesh</a></p>
  <p> Star this repository if you found it helpful!</p>
</div>

---

## Contact

- **GitHub**: [@Rakesh-ai-ds](https://github.com/Rakesh-ai-ds)
- **Project Link**: [https://github.com/Rakesh-ai-ds/hand_digit_recognition_cnn](https://github.com/Rakesh-ai-ds/hand_digit_recognition_cnn)

---
