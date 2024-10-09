# Instructions Documentation

## a) How I Approached the Solution

1. **Understanding the Requirement**:  
   The goal was to perform text analysis on articles stored in `.txt` files. The text analysis includes sentiment analysis, readability metrics, and word statistics.

2. **Directory Structure**:
   - Each article's content is stored in `.txt` files inside the `source/` folder.
   - Stopwords are located in the `StopWords/` directory.
   - Positive and negative words for sentiment analysis are stored in the `MasterDictionary/` directory.

3. **Text Preprocessing**:
   - Loaded the text from each `.txt` file.
   - Cleaned the text by removing punctuation and converting it to lowercase.
   - Tokenized the text and removed stop words using a combination of NLTK stopwords and custom stopwords from the `StopWords/` directory.

4. **Sentiment Analysis**:
   - Used a set of positive and negative words loaded from the `MasterDictionary/` directory to calculate:
     - **Positive Score**: Count of positive words.
     - **Negative Score**: Count of negative words.
     - **Polarity Score**: Measure of sentiment polarity.
     - **Subjectivity Score**: Measure of subjectivity based on the ratio of positive and negative words to total words.

5. **Readability Metrics**:
   - Calculated the average sentence length (number of words per sentence).
   - Measured the percentage of complex words (words with more than two syllables).
   - Computed the **Gunning Fog Index** to assess readability difficulty.
   - Calculated the average number of syllables per word and the average number of words per sentence as additional readability metrics.

6. **Word and Pronoun Statistics**:
   - Counted the total number of words and calculated the average word length.
   - Measured the number of personal pronouns (like "I", "we", "my") in each article.

7. **Result Storage**:
   - All computed metrics were appended to a DataFrame for each article.
   - The DataFrame was saved as an Excel file (`output_analysis.xlsx`).

---

## b) How to Run the `.py` File to Generate Output

1. **Clone the Repository or Place Files in a Directory**:
   Ensure your project structure looks like this:
