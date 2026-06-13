# 📩 Email/SMS-SPAM-DETECTION Using NLP and Streamlit
This is an end-to-end Email/SMS Spam Detection project using Natural Language Processing (NLP) and Machine Learning. The model classifies a message as Spam or Ham (Not Spam) based on its content.


# 📥How to Get the Dataset

We used the SMS Spam Collection dataset from the UCI Machine Learning Repository. You can download it from here:

🔗 UCI SMS Spam Dataset

After downloading:

1.Extract the file if needed.

2.Rename it to spam.csv and place it in your project root directory (or wherever your code is loading it from).

# 🧹 Data Cleaning Steps

Before training the model, we cleaned the raw dataset using the following steps:

# 🔻 Dropping Unnecessary Columns

- The original dataset contained additional unnamed columns (such as Unnamed: 2, Unnamed: 3, and Unnamed: 4) that did not contain useful information.
- These irrelevant columns were removed during preprocessing.
- Only the following columns were retained:
  - **v1**: Label of the message (`spam` or `ham`)
  - **v2**: SMS message text

# 🧯 Removing Duplicates

- Removed any duplicate messages to prevent data leakage or bias in the model.

# 🔄 Renaming Columns

- Renamed:

  - v1 ➝ target

  - v2 ➝ text

# 🔢 Encoding Labels
- Converted the target column to numerical:

  - ham ➝ 0

  - spam ➝ 1

# ⚙️ Data Preprocessing
- Preprocesses raw text using:
  - Lowercasing
  - Tokenization
  - Stopword removal
  - Stemming
- Converts text to numerical data using TF-IDF
- Predicts message as Spam or Ham using Naive Bayes
- Real-time web interface built with Streamlit
- Displays:
  - Prediction result ✅🚨
  - Confidence level
  - Transformed text for learning/debugging

# 🛠️ Tech Stack
- Python 3.x
- streamlit
- Pandas, NumPy
- Scikit-learn
- NLTK
- Pickle

# 📁 Folder Structure
📦SMS-Spam-Detection

┣ 📄 SMS_Spam_Detection.ipynb # Full notebook code

┣ 📄 spam.csv # Dataset (if public)

┣ 📄 app.py # Streamlit App

┣ 📄 model.pkl # Trained ML model

┗ 📄 vectorizer.pkl # TF-IDF vectorizer

# 🛠️ How to Run Locally
- In Pycharm's treminal run this commands
# Install streamlit
pip install streamlit

# Run Streamlit App
streamlit run app.py
