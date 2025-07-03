# Customer Feedback Analyzer

## Overview
Customer Feedback Analyzer is a Python application that uses Natural Language Processing (NLP) to analyze customer feedback. It performs sentiment analysis and extracts key phrases to summarize what customers liked and disliked based on their feedback.

## Features
- **Sentiment Analysis**: Uses NLTK's VADER (Valence Aware Dictionary and sEntiment Reasoner) to classify feedback as positive, negative, or neutral.
- **Phrase Extraction**: Identifies and summarizes key noun phrases from feedback to highlight liked and disliked aspects.
- **Interactive Interface**: Accepts user input for feedback and provides a concise summary of sentiment and key points.

## Requirements
- Python 3.6 or higher
- NLTK library (`pip install nltk`)

## Installation
1. Clone or download the repository:
   ```bash
   git clone <repository-url>
   cd customer-feedback-analyzer
   ```
2. Install the required dependencies:
   ```bash
   pip install nltk
   ```
3. Run the script to automatically download required NLTK resources (`vader_lexicon`, `punkt`, `stopwords`, `averaged_perceptron_tagger`).

## Usage
1. Run the script:
   ```bash
   python customer_feedback_analyzer.py
   ```
2. Enter customer feedback when prompted.
3. The program will output:
   - The overall sentiment (positive, negative, or neutral) with a compound score.
   - A summary of liked and disliked aspects extracted from the feedback.

### Example
**Input:**
```
The product quality is excellent, and the customer service was very helpful. However, the delivery was slow and packaging was damaged.
```

**Output:**
```
Sentiment: neutral (Score: 0.12)
Summary of Customer Feedback:
Liked: product quality, customer service
Disliked: delivery, packaging
```

## Code Structure
- **CustomerFeedbackAnalyzer**: Main class handling sentiment analysis and summary generation.
  - `analyze_sentiment`: Performs sentiment analysis using VADER.
  - `generate_summary`: Extracts key noun phrases for liked and disliked aspects using NLTK's chunking and frequency analysis.
  - `analyze_feedback`: Combines sentiment analysis and summary generation.
- **main**: Entry point for user interaction.

## Dependencies
- **NLTK**: For sentiment analysis, tokenization, stopword removal, part-of-speech tagging, and chunking.
  - Downloads required NLTK data: `vader_lexicon`, `punkt`, `stopwords`, `averaged_perceptron_tagger`.

## Limitations
- Requires internet access on first run to download NLTK resources.
- Phrase extraction is based on simple noun phrase chunking and may not capture all nuances in complex feedback.
- Sentiment analysis is based on VADER, which may not handle sarcasm or context-specific sentiments perfectly.

## Future Improvements
- Enhance phrase extraction with more sophisticated NLP techniques (e.g., dependency parsing).
- Add support for batch processing of multiple feedback entries.
- Integrate with a web interface for easier user interaction.

## License
This project is licensed under the MIT License.