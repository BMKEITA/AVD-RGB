# AVD-RGB Description
AVD-RGB is a lightweight defense against adversarial patch attacks, leveraging **RGB spectral discontinuities** and **uncertainty estimation** to detect malicious perturbations in images. The method requires **no model retraining** and achieves real-time performance.
Key Features:
- **Training-free detection** (works with any pre-trained model)
- **Fast inference** (100+ FPS on consumer GPUs)
- **Interpretable results** with visualization masks
- **Comprehensive metrics** (confidence scores, patch sizes, etc.)

## Installation
```bash
git clone https://github.com/BMKEITA/AVD-RGB.git
cd AVD-RGB
pip install -r requirements.txt

## Requirements:

Python 3.10+

OpenCV, PyTorch, scikit-image

CUDA 11.3 (for GPU acceleration)
