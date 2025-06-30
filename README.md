# AVD-RGB: Adversarial Patch Detection via RGB Spectral Discontinuity

<img width="567" alt="image6" src="https://github.com/user-attachments/assets/82eec68a-a998-42fb-9e18-708bec0d5ba4" />


A lightweight, training-free defense against physical adversarial patches by analyzing RGB spectral discontinuity and uncertainty estimation. Achieves 82-100% detection rates on benchmark datasets.

## Key Features

- **Training-free**: No additional training data required
- **Real-time capable**: Processes images at 102 FPS
- **Dual detection**: Combines spectral analysis and uncertainty estimation
- **Physical-world robust**: Tested on APRICOT and ImageNet-Patch datasets
- **Interpretable outputs**: Visualizations and confidence scores

## Installation

```bash
git clone https://github.com/BMKEITA/AVD-RGB.git
cd AVD-RGB
pip install -r requirements.txt
**Requirements**
Python 3.10+
- OpenCV
- PyTorch
- scikit-image
- matplotlib
**Usage**
Basic Detection
from avd_rgb import AVDRGB_Detector
import cv2

# Initialize detector
detector = AVDRGB_Detector(use_spectral=True, use_uncertainty=True)

# Load image
image = cv2.cvtColor(cv2.imread("test.jpg"), cv2.COLOR_BGR2RGB)

# Detect adversarial patches
result = detector.detect(image)

print(f"Adversarial: {result['is_adversarial']}, Confidence: {result['confidence']:.2f}")
cv2.imwrite("detection.jpg", cv2.cvtColor(result['visualization'], cv2.COLOR_RGB2BGR))
