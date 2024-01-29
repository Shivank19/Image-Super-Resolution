# Image-Super-Resolution

### Implementation of a Generative Adversarial Network (GAN) based approach to Image Super Resolution (SR) based on the idea proposed by [Ledig et al.](https://arxiv.org/abs/1609.04802)


## Implementation Methodology

1. We first process the dataset using OpenCV. Images in the dataset are downsampled to 256x256 pixels size, which act as our high-resolution images, and then are placed in a folder ‘hr-images’. These downsampled images are further downsampled by 4x to 64x64 pixels size to act as low-resolution images and these images are stored in the ‘lr-images’ folder.
2. The Generator and Discriminator models are prepared as per the architecture and then combined into a single model called ‘gan-model’ along with the perceptual loss.
3. Low-resolution images are passed through the Generator which upsamples and gives Super-Resolved Images. The Discriminator distinguishes the High-Resolution images and back-propagates the GAN loss to train the Generator and the Discriminator further.

## Getting Started

Follow these steps to set up and run the project locally:

1. **Clone the Repository:** Clone this repository to your local machine using the following command
   ```bash
   git clone https://github.com/your-username/Image-Super-Resolution-SRGAN.git
2. **Create an environment:** Create virtual environment for the project
   ```bash
    python -m venv name_of_environment
3. **Activate the Environment:**
   ```bash
    name_of_environment\Scripts\activate
4. **Install Dependencies:** Navigate to the project directory and install the required dependencies using
   ```bash
   pip install -r requirements.txt


### Prepare the dataset
1. Download and Unzip the [MIRFLICKR25k dataset](https://press.liacs.nl/mirflickr/mirdownload.html)
2. Downsample the images to 256x256 to act as High-Resolution Images and 64x64 to be used as Low-Resolution Images. using the [_data_prep.py_](https://github.com/Shivank19/Image-Super-Resolution-SRGAN/blob/main/data_prep.py) file


### Train Your Model
1. Run each cell in the [_SRGAN.ipynb_](https://github.com/Shivank19/Image-Super-Resolution-SRGAN/blob/main/SRGAN.ipynb) File to set the model
2. The Final cell in the file starts model training.


### Test using a Trained Model
1. Run the [_srgan_test.ipynb_](https://github.com/Shivank19/Image-Super-Resolution-SRGAN/blob/main/srgan_test.ipynb) File.
2. Load the model to test. The model should be in _HDF5 format_
3. Add the correct path to the dataset in the appropriate line.
4. Run the final cell to see the output.


## Contributing

Contributions are welcome from the community! To contribute to Editopia, follow these steps:

1. Fork the repository.

2. Create a new branch for your feature/bugfix: `git checkout -b feature/new-feature`.

3. Commit your changes: `git commit -m 'Add new feature'`.

4. Push to the branch: `git push origin feature/new-feature`.

5. Create a pull request explaining your changes.
