## Overview
The primary objective is to build a system capable of generating realistic handwritten digits based on user-specified inputs. Whether you need a single "7" or a sequence like "2025," this project uses label conditioning to ensure the generator produces images matching the exact class requested.  
+1

### Key Features
Dual Architecture Support: Compare a fully-connected cGAN (speed-focused) with a convolutional CDCGAN (quality-focused).  

Interactive Web App: A Streamlit-based interface for real-time digit generation and multi-digit composition.  

Variational Output: Generate up to 8 unique stylistic variations for any given digit sequence.  

Performance Analytics: Detailed logs of training stability, loss behaviors, and epoch timings.  

## Model Comparison
<img width="569" height="282" alt="image" src="https://github.com/user-attachments/assets/d9238c8f-0a84-441f-99fa-6dd487763662" />
###cDCGAN:
<img width="720" height="481" alt="image" src="https://github.com/user-attachments/assets/961f6d5c-6db4-4538-b32a-187316382ac9" />
###cGAN
<img width="740" height="485" alt="image" src="https://github.com/user-attachments/assets/026c6bd2-9936-4be5-8779-b3074cdf563b" />
<img width="708" height="289" alt="image" src="https://github.com/user-attachments/assets/4bf5f690-bca9-49a2-bbdc-7224aeac8e32" />


## Technical Implementation
### Architecture Details
Generator: Uses transposed convolutions (CDCGAN) or dense layers (cGAN) to upsample latent noise (z) and labels (y) into images.  

Discriminator: Acts as a binary classifier using BCELoss to distinguish between real MNIST samples and generated fakes.  

Optimization: Trained using the Adam optimizer with a learning rate of 0.0002 and β=(0.5,0.999).  

### Streamlit Web Application
The deployment includes a dashboard where users can:

Select Model: Switch between CDCGAN for best quality or cGAN for faster inference.  

Input Digits: Enter any number sequence to be synthesized.  

Adjust Variations: Use a slider to generate multiple different "handwriting" styles for the same number.  

Export: Download the final synthesized image as a PNG. 

<img width="705" height="355" alt="image" src="https://github.com/user-attachments/assets/36ccd266-fce5-48d8-9332-f7ee4692d1f0" />


## Requirements
Python 3.x

PyTorch & Torchvision

Streamlit

NumPy & Matplotlib
