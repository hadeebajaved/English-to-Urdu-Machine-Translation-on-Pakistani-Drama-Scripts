# English-to-Urdu Drama Transcript Translation

![NLP Translation](https://img.shields.io/badge/NLP-Machine%20Translation-blue)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![Urdu NLP](https://img.shields.io/badge/Language-Urdu-green)

## 📝 Project Overview
This project evaluates and enhances English-to-Urdu machine translation quality for **Pakistani drama transcripts** using state-of-the-art NLP models. We fine-tune and compare two translation systems, achieving a **BLEU score of 58.92** on conversational Urdu text.

## 🎯 Key Features
- Fine-tuned **Helsinki-NLP/opus-mt-en-ur** for domain-specific (drama) translations
- Benchmarking against **facebook/m2m100_418M** model
- Comprehensive preprocessing pipeline for Urdu text normalization
- BLEU score evaluation using `sacrebleu`
- Handling informal, conversational language nuances

## 🛠️ Technical Implementation
### Models Used
1. **Base Model**: `Helsinki-NLP/opus-mt-en-ur`
2. **Comparison Model**: `facebook/m2m100_418M`

### Tech Stack
- Python 3.10+
- HuggingFace Transformers
- HuggingFace Datasets
- SacreBLEU
- Pandas (for data handling)

### Data Pipeline
1. **Dataset**: English-Urdu parallel corpus from Pakistani drama transcripts
   - Originally English transcripts with Urdu translations via YouTube API
2. **Preprocessing**:
   - Whitespace and special character removal
   - Text normalization (both languages)
   - Handling missing translations
   - Train-test split (90%-10%)
3. **Tokenization**: Using HuggingFace's tokenizers

## 📊 Results
| Metric          | Score  |
|-----------------|--------|
| BLEU Score      | 58.92  |
| Test Set Size   | 500    |

**Key Insight**: The model shows strong performance on informal Urdu despite the challenges of conversational language translation.
