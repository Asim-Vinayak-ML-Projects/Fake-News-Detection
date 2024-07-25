# Fake News Detection using ANN

## Introduction
This project aims to develop a machine learning model capable of detecting fake news articles. We used a dataset consisting of both true and fake news articles and built an Artificial Neural Network (ANN) to classify news articles as either true or fake.

## Methodology

### Data Collection
We utilized two CSV files: `True.csv` and `Fake.csv`, each containing the following columns:
- `title`
- `text`
- `subject`
- `date`

### Data Preprocessing
1. **Combining and Shuffling Data**: The title, text, and subject columns were concatenated to form a single text column.
2. **Labeling**: True news articles were labeled as `1` and fake news articles as `0`.
3. **Cleaning**: Special characters were removed, and text was converted to lowercase. Stop words were removed, and words were stemmed using the PorterStemmer.
4. **Vectorization**: The text data was transformed into numerical features using TfidfVectorizer with a maximum of 5000 features.

### Model Training
An ANN was constructed with the following architecture:
- Input Layer: 512 units, ReLU activation
- Hidden Layers: 128, 64, 32, and 16 units with ReLU activation
- Output Layer: 1 unit with sigmoid activation

The model was trained using the Adam optimizer and binary cross-entropy loss. Early stopping was implemented to avoid overfitting.

## Results
### Model Performance
The ANN model achieved high accuracy in both training and validation phases. Below is a summary of the model's performance:

- **Training Accuracy**: ~99.9%
- **Validation Accuracy**: ~99.2%

## Results

### Evaluation Metrics
- **Confusion Matrix**:
  
  ```plaintext
  |                | Predicted Fake | Predicted True |
  |----------------|----------------|----------------|
  | Actual Fake    | 5896           | 27             |
  | Actual True    | 23             | 5279           |
This matrix provides a clear depiction of true positives, true negatives, false positives, and false negatives.

### Evaluation Metrics
- **Confusion Matrix**: Provided a clear depiction of true positives, true negatives, false positives, and false negatives.
- **Accuracy Score**: Demonstrated the overall correctness of the model.
- **ROC AUC Score**: Illustrated the model's ability to distinguish between classes.

### Visualizations
1. **Distribution of News Article Lengths**:
 ![image](https://github.com/user-attachments/assets/b25f29f4-4ec7-42e8-bcb6-71875f8571a3)


2. **Training and Validation Accuracy**:
 ![image](https://github.com/user-attachments/assets/c639c695-4c65-4b48-b073-c72a7a01f547)

2. **Training and Validation Accuracy**:
![image](https://github.com/user-attachments/assets/4e4a15da-0b57-4ac1-99c9-357eee7e81ab)



## Analysis
The results indicate that the model performs exceptionally well in distinguishing between true and fake news articles. The high accuracy and ROC AUC scores suggest that the model is both precise and robust.

### Conclusion
Our ANN model for fake news detection proves to be highly effective. Future work may involve:
- Experimenting with different text vectorization techniques such as Word2Vec or transformer-based embeddings.
- Fine-tuning the ANN architecture and hyperparameters.
- Expanding the dataset to include more diverse sources of news articles.

## How to Use
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/fake-news-detection.git
   cd fake-news-detection
