# Poem Sentiment Dataset Documentation

## 1. Metadata Card

| Field | Content |
| :--- | :--- |
| **Contributor** | Tang Yiwen |
| **Data Source** | Kaggle Poem Sentiment Collection ("https://huggingface.co/datasets/google-research-datasets/poem_sentiment") |
| **Domain/Category** | Literature / Sentiment Analysis |
| **Language** | English |
| **Data Scale** | 104 poetic text records, file size 4.56 KB |
| **File Format** | .csv |

## 2. Dataset Introduction

### 2.1 Dataset Content
This dataset contains 104 English poetry short verses and their corresponding emotion labels. Each record is stored in a structured format, with explanations of the core fields as follows:
- id: index of the example
- verse_text: The text of the poem verse
- label: The sentiment label. Here
0 = negative
1 = positive
2 = no impact
3 = mixed (both negative and positive)

### 2.2 Dataset Characteristics
1. Tag distribution characteristics: There are natural distribution differences among tag categories, with tag 2 accounting for the highest proportion (66.35%), and the proportions of tag 0 (18.27%) and tag 1 (15.38%) being relatively balanced, which is consistent with the diversity of emotional expressions in poetry texts;
2. Text length characteristics: The length of a single poetry text ranges from 9 to 75 characters, with an average length of 37.57 characters and a median of 37 characters. There are no invalid texts that are too long or too short, which is suitable for short-sentence sentiment analysis scenarios;
3. Data quality characteristics: The dataset has no missing values, no garbled characters, and no duplicate records. All text fields are grammatically correct English expressions, and no additional data cleaning is required for model training or analysis.

### 2.3 Data Acquisition Method
This dataset was obtained by downloading raw data from the public dataset google-research-datasets/poem_sentiment on the Hugging Face platform. After undergoing steps such as field filtering (retaining fields related to text and sentiment labels), data deduplication, and removal of invalid records, 104 valid records were finally extracted to ensure the representativeness and usability of the data.

### 2.4 Intended Research Uses
1. Training of sentiment classification models: Using `verse_text` as input features and `label` as the target variable, it can be used to train lightweight text sentiment classification models (such as Naive Bayes, small CNNs), which are suitable for sentiment recognition scenarios of short texts like poems;
2. Linguistic analysis of poetic emotions: Explore the linguistic features of emotional expression in English poetry (such as word choice, sentence structure), and compare the differences in poetic creation styles corresponding to different emotion labels (0/1/2);
3. Research on label imbalance optimization: Based on the characteristics of uneven label distribution in the dataset, it can be used to verify the effectiveness of label balancing algorithms such as SMOTE and weight adjustment in short text sentiment analysis tasks;
4. Application of literary emotion mining: It can be used as a sub-dataset of the poetic emotion corpus to support literary research topics such as emotional trend analysis of classical/modern English poetry and identification of authors' emotional tendencies.