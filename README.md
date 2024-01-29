# Image-Super-Resolution

### Implementation of a Generative Adversarial Network (GAN) based approach to Image Super Resolution (SR) based on the idea proposed by [Ledig et al.](https://arxiv.org/abs/1609.04802)


## Implementation Methodology
1. We first process the dataset using OpenCV. Images in the dataset are downsampled to 256x256 pixels
size, which act as our high-resolution images, and then are placed in a folder ‘hr-images’. These
downsampled images are further downsampled by 4x to 64x64 pixels size to act as low-resolution images
and these images are stored in the ‘lr-images’ folder.
2. The Generator and Discriminator models are prepared as per the architecture and then combined
into a single model called ‘gan-model’ along with the perceptual loss.
3. Low-Resolution Images are passed through the Generator which upsamples and gives Super-Resolved
Images. The Discriminator distinguishes the High Resolution images and back-propagates the GAN
loss to further train the Generator and the Discriminator.