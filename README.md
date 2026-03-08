# 🧠 BERT News Topic Classifier (AG News Dataset)

## 📌 Objective of the Task

The objective of this project is to build a Natural Language Processing (NLP) model that automatically classifies news headlines into topic categories.

A pre-trained transformer model **BERT (bert-base-uncased)** is fine-tuned on the **AG News dataset** to classify headlines into four categories:

- World
- Sports
- Business
- Science / Technology

The goal is to demonstrate how **transfer learning with transformers** can be applied to solve real-world text classification problems.

---

## 📊 Dataset Used

The project uses the **AG News Dataset**, available through the Hugging Face `datasets` library.

Dataset Characteristics:

- 120,000 training samples
- 7,600 test samples
- Each sample contains:
  - News headline text
  - Corresponding topic label

### Categories

| Label | Category |
|------|------|
| 0 | World |
| 1 | Sports |
| 2 | Business |
| 3 | Sci/Tech |

---

## ⚙ Methodology / Approach

The following steps were used to build the news classification system:

### 1️⃣ Dataset Loading
The AG News dataset was loaded using the Hugging Face `datasets` library.

### 2️⃣ Text Tokenization
News headlines were tokenized using the **BERT tokenizer** (`bert-base-uncased`) to convert text into numerical input format required by the model.

### 3️⃣ Model Fine-Tuning
A pre-trained **BERT transformer model** was fine-tuned using the Hugging Face `Trainer` API.

Key training configurations included:

- Learning Rate: `2e-5`
- Batch Size: `16`
- Epochs: `2`
- Maximum sequence length: `128`

### 4️⃣ Model Evaluation
The model was evaluated using:

- **Accuracy**
- **F1-score**

These metrics help measure how well the classifier predicts the correct news category.

### 5️⃣ Prediction Pipeline
A Hugging Face `pipeline` was created to allow real-time classification of new news headlines.

---

## 📈 Key Results / Observations

- The fine-tuned BERT model achieved **high accuracy and strong F1-score** on the AG News test dataset.
- Transformer models demonstrate excellent performance in text classification tasks due to their contextual language understanding.
- Transfer learning significantly reduces training time compared to building models from scratch.
- The trained model can successfully classify unseen news headlines into appropriate categories.

---

## 🧪 Example Prediction

Input headline:

```
Apple releases new AI powered laptop chip
```

Predicted category:

```
Sci/Tech
```

---

## 🛠 Technologies Used

- Python
- Hugging Face Transformers
- Hugging Face Datasets
- PyTorch
- Scikit-learn
- Google Colab

---

## 🎓 Skills Gained

- NLP using Transformer models
- Transfer learning & fine-tuning
- Text tokenization with BERT
- Model evaluation with accuracy and F1-score
- Building text classification pipelines

---

## 🚀 Conclusion

This project demonstrates how transformer-based models like **BERT** can be fine-tuned for efficient and accurate text classification tasks. Using transfer learning with pre-trained language models allows developers to build powerful NLP systems with relatively small effort and computational cost.

The approach used in this project can be extended to other real-world applications such as sentiment analysis, spam detection, and document categorization.
