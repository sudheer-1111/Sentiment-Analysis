
# Sentiment Analysis Models

This project performs sentiment analysis on text using three different models:
- **TextBlob** (Lexicon-based approach)
- **VADER (Valence Aware Dictionary and sEntiment Reasoner)** from **NLTK** (Lexicon-based, optimized for social media texts)
- **Hugging Face Transformers** (Deep learning-based model for more context-aware sentiment analysis)

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Models Used](#models-used)
- [Example Output](#example-output)
- [File Structure](#file-structure)
- [License](#license)

## Installation

To run this project, you will need to have Python 3.x installed. Follow these steps to set up the environment:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Sentiment-Analysis-Models.git
   cd Sentiment-Analysis-Models
   ```

2. Install the required dependencies by running:
   ```bash
   pip install -r requirements.txt
   ```

   This will install:
   - `textblob` (for lexicon-based sentiment analysis)
   - `nltk` (for VADER sentiment analysis)
   - `transformers` (for Hugging Face models)
   
3. Download additional resources for VADER (NLTK):
   ```bash
   python -m nltk.downloader vader_lexicon
   ```

## Usage

Once the setup is complete, you can run the sentiment analysis on predefined or custom text. Use the following command to analyze sentiment:

```bash
python sentiment_analysis.py
```

You can modify the `texts` array in the script to add your own sentences for analysis.

### Models Used:

1. **TextBlob**:
   - A lexicon-based sentiment analysis tool that computes **polarity** and **subjectivity**.
   - Polarity ranges from `-1` (negative) to `1` (positive).
   - Subjectivity ranges from `0` (objective) to `1` (subjective).

2. **VADER (NLTK)**:
   - A rule-based model specially optimized for sentiment analysis in social media texts.
   - The **compound score** determines the overall sentiment, ranging from `-1` (most negative) to `1` (most positive).

3. **Hugging Face Transformers**:
   - A pre-trained **DistilBERT** model fine-tuned on the **SST-2** dataset for sentiment analysis.
   - Provides a binary classification of **positive** or **negative** sentiment along with a **confidence score**.

### Example Output

Running the script on predefined text will output results from all three models:

```bash
Sentiment Analysis Results for: "I don't hate this movie, it's actually quite good!"

--- TextBlob ---
Sentiment: Positive
Polarity: 0.5, Subjectivity: 0.6

--- VADER (NLTK) ---
Sentiment: Positive
Compound Score: 0.6044

--- Hugging Face Transformers ---
Sentiment: POSITIVE
Confidence Score: 0.999847
```

### File Structure

The project directory contains the following files:

```bash
.
├── sentiment_analysis.py  # Main script that runs sentiment analysis using all three models
├── requirements.txt       # Dependencies required to run the project
├── README.md              # Documentation for the project
└── .gitignore             # Ignored files for Git
```

### License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
