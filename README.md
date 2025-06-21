# Email-Spam-Classifier

A web application that classifies emails or SMS messages as **Spam** or **Not Spam** using machine learning and natural language processing (NLP). Built with Streamlit, this app allows users to input a message and instantly get a prediction.

## Dataset

The model is trained on the [spam.csv](./spam.csv) dataset, which contains thousands of labeled SMS messages as either 'ham' (not spam) or 'spam'.

## Features
- Text preprocessing (tokenization, stopword removal, stemming)
- TF-IDF vectorization
- Multinomial Naive Bayes classifier
- Simple and interactive web interface (Streamlit)
- Ready for deployment (Heroku compatible)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd Email-Spam-Classifier
   ```

2. **Install dependencies**
   It is recommended to use a virtual environment.
   ```bash
   pip install -r requirements.txt
   ```
   
   Additionally, you may need to download NLTK resources:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   ```

## Usage

1. **Run the Streamlit app**
   ```bash
   streamlit run app.py
   ```
2. Open your browser and go to the local URL provided by Streamlit (usually http://localhost:8501).
3. Enter an email or SMS message in the text area and click 'Predict' to see if it is spam or not.

## Deployment

This app is ready for deployment on platforms like Heroku.

- **Procfile**: Specifies the command to launch the app.
- **setup.sh**: Sets up Streamlit configuration for deployment.

**To deploy:**
1. Make sure all files are in your repository (`app.py`, `requirements.txt`, `procfile`, `setup.sh`, model files, etc.).
2. Push to your Heroku app or similar PaaS.

## File Descriptions
- `app.py`: Main Streamlit application for spam classification.
- `Main-file.ipynb`: Jupyter notebook for data exploration, preprocessing, and model training.
- `spam.csv`: The dataset used for training/testing.
- `MNB.pkl`: Trained Multinomial Naive Bayes model.
- `tf.pkl`: Trained TF-IDF vectorizer.
- `voting.pkl`: (Optional) May contain an ensemble model (not used in the current app).
- `inedx.html`: (Unused) HTML template, not required for Streamlit app.
- `procfile`: Deployment command for Heroku.
- `setup.sh`: Streamlit server configuration for deployment.
- `requirements.txt`: Python dependencies.

## Acknowledgements
- [UCI SMS Spam Collection Dataset](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection)
- [Streamlit](https://streamlit.io/)
- [NLTK](https://www.nltk.org/)
- [scikit-learn](https://scikit-learn.org/)

---

**Created by Bappy Ahmed**