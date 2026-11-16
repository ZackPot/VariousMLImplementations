# ML Implementations in Python

This project should serve as a template for various ML algorithms. The project uses tensorflow and is a collection of different training code for different model architectures.


# Model Architectures

- U-Net 
- LSTM
- MLP with Embeddings
- WaveNet

# The CNN Encoder/Decoder

This model uses 2 skip connections, leaky relu and batchnormalization to predict images of shoes from edges. The model also has a combination of ssim + mae loss to retain detail. The model architecture is like so:

- **Encoder**
- 2 Conv2D (feature reconnection)
- 1 MaxPooling (downscale)
- 2 Conv2D
- 1 MaxPooling


- **Bottleneck**
- 2 Conv2D


- **Decoder**
- 1 UpScaling2D (upscaling)
- Skip Connection
- 2 Conv2D
- 1 UpScaling2D 
- Skip Connection  
- 2 Conv2D 
  
- Output Sigmoid Activation

# MLP with Embeddings
This model uses a custom lookup table for SMILEs medicine, which it then feeds into a MLP (basically a normal model) to determine their pIC50 (the drug's potency). The model architecture is like so:

- Input
- Batch Normalization
- Dense 256
- Dense 128
- Output

The dataset can be found at https://www.kaggle.com/datasets/yanmaksi/big-molecules-smiles-dataset.
