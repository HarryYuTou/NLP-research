# NLP + Computer Vision Model for Multi-Label Classification

This repository contains a project that integrates **Natural Language Processing (NLP)** and **Computer Vision** for multi-modal classification tasks. The model is built to predict multiple labels using image data processed through **ResNet-18** and textual data processed using **BERT-base-uncased**. The architecture combines features from both modalities and classifies inputs into one of 6 classes.

## **Background**

This project focuses on creating a multi-modal classification model that leverages both **Natural Language Processing (NLP)** and **Computer Vision** techniques. The aim is to classify inputs based on both **textual data** and **visual data**, combining the strength of language models like **BERT-base-uncased** for text and **ResNet-18** for images. The model is designed to perform multi-label classification, where each input may be associated with multiple classes. This approach has wide-ranging applications, from content moderation to understanding multi-faceted data sources like multimedia posts on social platforms.

## Project Structure

- **Model Architecture**: The model uses **ResNet-18** for processing images and **BERT-base-uncased** for processing text. These features are combined and passed through a final classifier to predict the labels.
- **Dataset**: The project utilizes the **MMH150K** dataset with 3 available labels for training. The model is designed to predict labels based on the given input.
- **Multimodal Fusion**: The model extracts image features (512 dimensions from ResNet-18) and text features (768 dimensions from BERT). These features are concatenated and passed through fully connected layers for classification.

## Installation

To run this project, clone the repository and install the required dependencies:
https://github.com/HarryYuTou/NLP_n_Computer-Vision


## Dataset

The **MMH150K** dataset consists of 150,000 samples with 3 available labels. The dataset includes both textual and image data.

### Preprocessing

- **Text Preprocessing**: The text is tokenized using the **BERT tokenizer**, with padding and truncation applied to fit the input size for the BERT model.
- **Image Preprocessing**: The images are resized and normalized according to the **ResNet-18** model requirements.

## Model Details

- **ResNet-18**: The ResNet-18 model is used to process images and extract a 512-dimensional feature vector.
- **BERT-base-uncased**: The BERT-base-uncased model is used to process text and extract a 768-dimensional feature vector.
- **Classifier**: The combined features from both modalities are passed through a fully connected layer (512 + 768) to predict 6 output classes.

## **Output**

The model is designed to predict multiple labels for each input sample based on text and image inputs. After processing the image with **ResNet-18** and the text with **BERT-base-uncased**, the model outputs probabilities for each of the six defined labels. The output will consist of the **top 3 predicted labels** for each input, ranked by the model’s confidence.

## **Summary**

This project demonstrates the power of multi-modal learning by combining **BERT** for text and **ResNet-18** for images. Through this architecture, the model can predict multiple labels for a given input, which could be an image-text pair such as a social media post. The use of **multi-label classification** makes this approach suitable for scenarios where each input can belong to more than one class, enhancing its flexibility and real-world applicability. Although the current implementation yields promising results, further improvements can be made by addressing class imbalances and fine-tuning the model for specific tasks or domains.
