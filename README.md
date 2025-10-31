# Model Stealing Attack

Implemented By:
Ahrar Bin Aslam and Muhammad Mubeen Siddiqui

This repository contains our implementation for a model stealing attack as part of the TML course (Assignment 2). The goal was to replicate the functionality of a black-box encoder exposed via an API and protected using B4B noising. We approached this by querying the API with images from a known dataset and training our own encoder to match the returned embeddings.

We primarily used a modified ResNet18 architecture and trained it using a combination of cosine similarity and MSE loss to closely align with the victim model’s embeddings. Our final model achieves strong performance, with an L2 distance of 6.19 to the target encoder. We also experimented with a shadow encoder and meta-classifier setup inspired by BESA to simulate and reverse various defenses, though this path was limited by compute resources.

---

## Try it out

To try it out:
1. Clone this repository.
2. Launch the notebook Model Stealing TML25_A2_16.ipynb in Google Colab.
3. Make sure to insert the correct TOKEN, SEED, and PORT.

> Full pipeline runs in ~15 minutes on Colab’s free GPU.
