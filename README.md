Named Entity Recognition (NER) Case Study
Objective
The goal of this case study is to build a Named Entity Recognition (NER) system that can identify and classify entities such as names, locations, organizations, and other key categories from text.
For this task, I experimented with two different approaches:
Bi-LSTM + CRF Model
BERT-based Model
The performance of both methods was compared to evaluate their effectiveness in sequence labeling tasks.
About the Dataset
File: ner_dataset.csv
Columns:
Sentence # → Index mapping each word to its respective sentence.
Word → The word/token in the sentence.
POS → Part-of-speech tag for the word (not used in this case study).
Tag → Named Entity Recognition label for the word.
For the purpose of this study, only Word and Tag columns were used. Each sentence is represented as a sequence of words with corresponding NER tags.
Methods Implemented
1. Bi-LSTM + CRF Model
Bi-LSTM captures contextual information in both forward and backward directions.
CRF (Conditional Random Field) is applied on top to model dependencies between output labels, ensuring valid tag sequences.
This architecture is effective for sequence labeling tasks where the tag of a word often depends on its neighbors.
2. BERT-based Model
Leveraged BERT (Bidirectional Encoder Representations from Transformers) for contextual embeddings.
BERT captures deep bidirectional context at the word and sentence level.
A classification layer was added on top of BERT to predict NER tags for each token.
Compared to Bi-LSTM + CRF, BERT reduces the need for handcrafted features and typically provides higher accuracy.
