# Image Captioning using ResNet50 and Attention

## Overview
This repository contains an Image Captioning model developed during my Summer Internship at the Indian Institute of Technology, Guwahati (IITG). The system takes an image as input and automatically generates a descriptive natural language sentence explaining the visual content.

## Model Architecture
The project utilizes a standard Encoder-Decoder architecture enhanced with an attention mechanism:
* **Encoder:** A pre-trained **ResNet50** CNN model is used to extract high-level feature vectors from the input images. To optimize training efficiency, these image features were pre-extracted and stored.
* **Decoder:** An **LSTM** (Long Short-Term Memory) recurrent neural network generates the descriptive text word by word.
* **Attention Mechanism:** **Bahdanau Attention** is implemented within the decoder, allowing the model to focus on specific, relevant parts of the image as it predicts each subsequent word in the sequence.

## Dataset
* **Flickr8k Dataset:** The model was trained and evaluated using the standard Flickr8k dataset, which contains 8,000 images, each paired with 5 different reference captions.

## Evaluation Metrics
To comprehensively validate the model's performance and accuracy against human-generated captions, the following NLP metrics were used:
* **BLEU** (Bilingual Evaluation Understudy)
* **METEOR** (Metric for Evaluation of Translation with Explicit ORdering)
* **ROUGE_L** (Recall-Oriented Understudy for Gisting Evaluation)
* **CIDEr** (Consensus-based Image Description Evaluation)
* **SPICE** (Semantic Propositional Image Caption Evaluation)

## Tech Stack
* Python
* PyTorch / TensorFlow *(Adjust this based on what you actually used)*
* Google Colab
