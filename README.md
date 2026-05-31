# ML Implementations in Python

This project should serve as a frame of reference for anybody who wants to code ML. It is made in kaggle using tensorflow and is a collection of different training code for different model architectures. The project can be found here at https://www.kaggle.com/code/zacharypotishko/various-ml-implementations-in-tensor-flow


# Model Architectures

Currently, we have:
- U-Net 

We want to develop:
- LSTM
- MLP with Embeddings
- WaveNet

# The CNN Encoder/Decoder

This model uses 2 skip connections, leaky relu and batchnormalization to predict images of shoes from edges. The model also has a combination of ssim + mae loss to retain detail. The model architecture is like so:

- **Encoder**
- 2 Conv2D (feature recongition) #1
- 1 MaxPooling (downscale) #2
- 1 Conv2D #3
- 1 Conv2D #4
- 1 MaxPooling #5

- **Bottleneck**
- 2 Conv2D #6

- **Decoder**
- 1 UpScaling2D (upscaling) #7
- A skip connection between #6 and #3. #8
- 2 Conv2D #9
- 1 UpScaling2D #10
- Skip Connection between #10 and the 2nd layer of #1. #11
- 2 Conv2D #12
  
- Output Sigmoid Activation
