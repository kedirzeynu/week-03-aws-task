## Week-03-aws-task: SMS Spam Detector

A small machine-learning project that classifies SMS messages as `spam` or `ham` (not spam) using TF-IDF features and Multinomial Naive Bayes.

## Project Structue

week-03-aws-task/
├── spam_filter.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    └── .gitkeep

## Open in Google Colab

`https://colab.research.google.com/github/kedirzeynu/week-03-aws-task/blob/main/spam_filter.ipynb`


## Dataset

SMS Spam Collection, UCI Machine Learning Repository:
https://archive.ics.uci.edu/dataset/228/sms+spam+collection

The dataset is downloaded automatically by the notebook into `data/` at runtime.

## How to run locally

1. Clone the repository.
2. Create and activate a virtual environment (optional but recommended).
3. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open `spam_filter.ipynb` in Jupyter or VS Code and run all cells.

## Method

- Split the dataset into training and test sets (80/20, stratified).
- Convert text to TF-IDF features.
- Train a Multinomial Naive Bayes classifier.
- Report accuracy, precision, recall, classification report, and confusion matrix.
- Test five hand-written messages.

## Results

### Model Evaluation

| Metric | Result |
|---|---|
| Accuracy | 0.9605 |
| Spam precision | 1.0000 |
| Spam recall | 0.7047 |

### Tricky Message Predictions

| # | Test Message | Predicted | Expected | Explanation |
|---|---|---|---|---|
| 1 | Cl@im your fr33 g1ft card now | spam/ham | spam | Unusual spelling and character substitutions |
| 2 | Not free, just confirming lunch at 1pm | spam/ham | ham | Misleading keyword and negation |
| 3 | Congratulations! You have won a free prize. Claim now! | spam/ham | spam | Common spam phrases |
| 4 | Your account is blocked. Verify your details immediately. | spam/ham | spam | Urgent language and suspicious request |
| 5 | Hi, could you please send me the meeting notes? | spam/ham | ham | Ordinary conversational message |

## What I Learned

This project helped me understand how TF-IDF converts text messages into numerical features and how Multinomial Naive Bayes uses these features to classify messages as spam or legitimate.
I learned how to evaluate a machine learning model using accuracy, precision, recall, and a confusion matrix.