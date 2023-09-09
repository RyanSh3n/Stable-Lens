# Stable-Lens
Stable Lens is an Image captioning model based on CLIP and Stablelm. Given an image, it uses the CLIP encoder to extract visual features in the form of a CLIP embedding. Then a MLP is used as a mapping network which maps the CLIP embedding into a vector inside the Stablelm tokenizer's latent space. Finally, the output from the mapping network is used as a prefix which is then fed into Stabelm to create an caption.

The prefix idea was based on the paper "ClipCap: CLIP Prefix for Image Captioning [https://arxiv.org/abs/2111.09734]". Additionally the pickle files used in the notebook were generated from https://github.com/rmokady/CLIP_prefix_caption/blob/main/parse_coco.py
