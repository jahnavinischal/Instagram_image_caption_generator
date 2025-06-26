# 🖼️ Instagram Image Caption Generator using Attention Mechanism

This project builds an AI model that automatically generates captions for Instagram-style images using deep learning. It leverages a Convolutional Neural Network (CNN) for image feature extraction and a Recurrent Neural Network (RNN) with Bahdanau Attention to generate natural language descriptions.

---

## 🧠 Overview

This image captioning system:
- Extracts visual features using a pretrained **InceptionV3** model.
- Uses **Bahdanau Attention** to selectively focus on parts of the image while generating each word.
- Trains an encoder-decoder model to produce meaningful and human-like captions.

---

## 📂 Dataset

- **Images**: Instagram-style user images.
- **Captions**: Stored in a CSV with columns like `Image File` and `Caption`.

Dataset source:  
📦 [Instagram Images with Captions on Kaggle]([https://www.kaggle.com/datasets/programmerrdai/ozone-layer](https://www.kaggle.com/datasets/prithvijaunjale/instagram-images-with-captions/data))  

---

## 🏗️ Architecture

### ➕ Encoder
- **InceptionV3** pretrained on ImageNet
- Extracts 2048-dim feature vectors from images

### 🎯 Attention
- Implements **Bahdanau soft attention** to focus on relevant image features for each word in the caption

### 📝 Decoder
- **Embedding Layer** → **LSTM** → **Dense Layer (softmax)**

### 🔄 Overview Diagram

```text
[Image] → [InceptionV3] → [Feature Vector] ─┐
                                            │
                                     [Bahdanau Attention] ← [LSTM State]
                                            │
         [Caption Input] → [Embedding] → [LSTM Decoder] → [Next Word]

```

---

## 📊 Evaluation

For evaluation BLEU score was used with average value around 0.5, which is good.

---

## 🔮 Future Work
- Use Transformer-based captioning models 
- Integrate Instagram API for real-time captioning

