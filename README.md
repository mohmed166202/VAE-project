# 🖼️ VAE/CVAE Image Generation Project

<div align="center">
  <img src="https://img.shields.io/badge/python-3.6%2B-blue" alt="Python">
  <img src="https://img.shields.io/badge/TensorFlow-2.x-orange" alt="TensorFlow">
  <img src="https://img.shields.io/badge/Keras-2.x-red" alt="Keras">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
</div>

## 📝 Description
This project implements both Variational Autoencoder (VAE) and Conditional VAE (CVAE) models for image generation. Originally developed in Google Colab, it has been adapted for local execution in VS Code with support for custom datasets.

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/vae-cvae-project.git
cd vae-cvae-project

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

data/
├── MAG/    # Put Class 1 images here (*.jpg, *.png)
└── ME/     # Put Class 2 images here


python vae_cvae.py

🛠️ Configuration Options
You can modify these parameters in the code:

Parameter	Location	Default Value	Description
TARGET_SIZE	load_and_preprocess_images()	(32, 32)	Output image size (width, height)
INTERMEDIATE_DIM	main() function	256	Size of hidden layer
LATENT_DIM	main() function	64	Dimension of latent space
EPOCHS	train_model() call	5	Number of training epochs
BATCH_SIZE	train_model() call	16	Images per training batch

vae-cvae-project/
│
├── data/                   # Image datasets (create this folder)
│   ├── MAG/                # Class 1 images
│   └── ME/                 # Class 2 images
│
├── outputs/                # Generated images (auto-created)
│
├── vae_cvae.py            # Main implementation file
├── README.md              # This documentation file
└── requirements.txt       # Python dependencies

🔧 Dependencies
The requirements.txt file contains:
tensorflow>=2.0
keras>=2.0
numpy>=1.0
pandas>=1.0
matplotlib>=3.0
pillow>=8.0

🎨 Sample Usage
Generating Images
After launching the program:

Choose option 1 (VAE) or 2 (CVAE)

Enter number of images to generate (1-10)

View results in matplotlib window

Example output:
Select an option:
1. Generate random VAE images
2. Generate class-conditioned CVAE images
3. Exit
> 2
How many images to generate? (1-10): 3
Generating 3 images...

