# Spam Mail Detector

## Project Overview
A machine learning solution that identifies spam emails with **96.7% accuracy**, leveraging natural language processing and classification algorithms for reliable message filtering.

---

### Core Features
- **TF-IDF Vectorization**: Optimized text feature extraction
- **Logistic Regression Classification**: Efficient binary prediction model
- **Data Foundation**: 5,572 messages from the SMS Spam Collection Dataset

---

## Technical Implementation

### Pipeline
1. **Data Preparation**:
   - Null value handling
   - Label encoding (spam=0, ham=1)
2. **Feature Engineering**:
   - TF-IDF vectorization with stop word removal
3. **Model Development**:
   - 80/20 train/test split
   - Logistic Regression implementation

### Performance Metrics
| Metric | Score |
|--------|-------|
| Training Accuracy | 96.7% |
| Testing Accuracy | 96.6% |

---

## Environment Setup

### Requirements
- Python 3.8+
- pandas | numpy | scikit-learn

```bash
git clone https://github.com/Arpita-Panigrahi/Spam-mail-detector.git
pip install -r requirements.txt
```

---

## Implementation Example

```python
# Initialize classifier
vectorizer = TfidfVectorizer(min_df=1, stop_words='english')
model = LogisticRegression()

# Classify message
sample_email = ["Congratulations! You've won a $500 Amazon gift card"]
features = vectorizer.transform(sample_email)
prediction = "Spam" if model.predict(features)[0] == 0 else "Legitimate"
```

---

## Technical Rationale

- **TF-IDF**: Prioritizes discriminative terms in classification
- **Logistic Regression**: Provides optimal performance for text classification tasks
- **Modular Architecture**: Ensures maintainability and extensibility

---

## Development Roadmap

- Cross-validation implementation
- Docker containerization
- Comprehensive evaluation metrics
- API integration for production deployment

---

## Contribution Guidelines

Seeking contributions in:
- Performance optimization
- Test case expansion
- Documentation enhancement

---

**License**: MIT  
**Developer**: Arpita  
