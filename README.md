# monet2photo-cyclegan
This mini-project implements a CycleGAN model to perform unpaired image-to-image translation, transforming Monet-style paintings into photorealistic images using TensorFlow and Keras.

## Dataset
The dataset used is the **[gan-getting-started](https://www.kaggle.com/competitions/gan-getting-started)** dataset from Kaggle. It includes two unpaired sets of 256x256 JPEG images:
- `monet_jpg/`: Monet-style paintings
- `photo_jpg/`: Real photographs

## Model
We use the CycleGAN architecture consisting of:
- Two Generators: Monet → Photo and Photo → Monet
- Two Discriminators: One for each domain
- Key losses used:
  - **Adversarial Loss**
  - **Cycle-Consistency Loss**
  - **Identity Loss**

These losses help the model learn both realistic translation and preserve semantic content between domains.

##  Setup
To run the notebook:
```bash
!pip install git+https://github.com/tensorflow/examples.git
!pip install kaggle
