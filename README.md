# Stable-Lens: Image Captioning with CLIP and Stablelm

Stable Lens is an image captioning model that leverages the power of CLIP and Stablelm. This model generates descriptive captions for images by combining visual features extracted using the CLIP encoder with Stablelm's text generation capabilities.

## How it Works

1. **CLIP Encoding**: Stable Lens begins by utilizing the CLIP encoder to extract rich visual features from the input image. These features are represented as a CLIP embedding, capturing the essence of the image.

2. **Mapping Network (MLP)**: To bridge the gap between the CLIP embedding and Stablelm's text generation capabilities, a Multi-Layer Perceptron (MLP) serves as a mapping network. This MLP transforms the CLIP embedding into a vector within the Stablelm tokenizer's latent space.

3. **Stablelm for Captioning**: The output from the mapping network becomes a prefix, which is then fed into Stablelm. Stablelm, a powerful language model, takes this prefix and generates a coherent and contextually relevant caption for the given image.

### Sample Generated Captions from COCO Images
<img width="475" alt="image" src="https://github.com/RyanSh3n/Stable-Lens/assets/45503218/e0b3edc1-1a97-46d1-9ebf-c9e7830dad23">

## References

- The idea of using a prefix for image captioning is inspired by the paper [ClipCap: CLIP Prefix for Image Captioning](https://arxiv.org/abs/2111.09734).

## Usage

To get started with Stable-Lens and reproduce the results, open the included Jupyter notebook (`Stable-Lens-Image-Captioning.ipynb`). 

### Notebook Contents

Inside the notebook, you will find:

- **Model Definition**: The notebook contains the model architecture definition, including the CLIP encoder, mapping network (MLP), and Stablelm configuration.

- **Model Training**: Scripts and code for training the Stable Lens model using your own dataset or pre-existing data.

- **Model Inference**: Code for generating image captions using the trained model. You can provide your own images for caption generation.

- **Model Evaluation**: Techniques for evaluating the model's performance, including the calculation of BLEU scores to measure the quality of generated captions.

The pickle files included in this repository contain CLIP embeddings alongside captions and were generated using the script found [here](https://github.com/rmokady/CLIP_prefix_caption/blob/main/parse_coco.py).
