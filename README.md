
# 📷 Image Captioning using CNNs and LSTMs (Flickr8k)

This project implements an **Image Captioning system** using deep learning techniques. The model is trained on the **Flickr8k dataset** and leverages **Convolutional Neural Networks (CNNs)** for image feature extraction and **Long Short-Term Memory (LSTM)** networks for generating natural language captions.

---

## 🧠 Project Overview

- **Task**: Automatically generate a textual description for a given image.
- **Approach**: Combines a CNN (e.g., VGG16/ResNet/DenseNet) as an encoder with an LSTM-based RNN as a decoder.
- **Dataset**: [Flickr8k](https://forms.illinois.edu/sec/1713398) - 8,000 images with five captions each.

---

## 📁 Repository Structure

```
flickr8k-image-captioning/
├── flickr8k-image-captioning-using-cnns-lstms.ipynb  # Main notebook
├── images/                                           # Sample results (optional)
├── models/                                           # Saved model checkpoints (optional)
└── README.md                                         # This file
```

---

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/flickr8k-image-captioning.git
   cd flickr8k-image-captioning
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   Required libraries include:
   - TensorFlow / Keras
   - NumPy
   - Pandas
   - Matplotlib
   - Seaborn
   - tqdm

3. **Download the Flickr8k dataset:**
   - [Request and download from here](https://forms.illinois.edu/sec/1713398)
   - Extract and place:
     - `Flickr8k_Dataset` folder (images) in your working directory.
     - `Flickr8k_text` folder (captions) alongside it.

---

## 🧩 How It Works

1. **Data Preprocessing:**
   - Clean and tokenize the captions.
   - Create a vocabulary and word-to-index mappings.
   - Extract image features using a pretrained CNN (VGG16/ResNet50/DenseNet201).

2. **Model Architecture:**
   - **Encoder**: CNN (pretrained on ImageNet) extracts a feature vector from the image.
   - **Decoder**: LSTM network generates a sequence of words based on the image embedding and previous words.

3. **Training:**
   - Trained using categorical cross-entropy loss.
   - Includes callbacks like EarlyStopping and ReduceLROnPlateau.

4. **Inference:**
   - Greedy decoding used for caption generation.
   - Generates natural language descriptions for unseen images.

---

## 📊 Results

- **Qualitative Results**: (Add sample image-caption pairs here)

| Image | Generated Caption |
|-------|-------------------|
| ![](images/img-1.png) | "A dog running through a field" |
| ![](images/img-2.png) | "Two children playing with a ball" |

---

## 🚀 To Run the Project

1. Open the Jupyter notebook:
   ```bash
   jupyter notebook flickr8k-image-captioning-using-cnns-lstms.ipynb
   ```

2. Execute the cells step by step:
   - Preprocess data
   - Extract features
   - Train the model
   - Generate captions

---

## 👤 Contributors

- **Your Name**  
  [LinkedIn](#) | [GitHub](#)

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
