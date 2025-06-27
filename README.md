# AI-Powered Job Matching & Interview Preparation Tool

An end-to-end NLP-based system to intelligently match resumes with job descriptions and help users prepare for interviews using state-of-the-art **transformer models**. This tool is ideal for students, job seekers, HR platforms, and resume-screening applications.

---

##  Key Objectives

- 🧾 **Match** resumes with job descriptions using semantic understanding.
- 🤖 **Leverage** advanced **BERT/Sentence-BERT** embeddings for natural language understanding.
- 📊 **Rank** job roles based on their similarity to candidate profiles.
- 🧠 **Prepare** users with potential interview questions (extension module).
- 🧪 **Experiment** with TF-IDF vs Embedding-based similarity approaches.

---

##  Core Capabilities

| Feature                        | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| ✅ Resume Parsing              | Input plain text or docx format resumes.                                   |
| ✅ Job Description Input       | Compare against multiple JD strings.                                       |
| ✅ Text Preprocessing          | Cleansing, tokenization, stopword removal, lemmatization.                  |
| ✅ TF-IDF Similarity           | Fast, interpretable keyword-based matching.                                |
| ✅ BERT Semantic Similarity    | Deep sentence embeddings using Sentence-BERT (`all-MiniLM-L6-v2`).         |
| ✅ Score Ranking               | Cosine similarity-based ranking of job relevance.                          |
| 🔜 Interview QA Generator     | Future module: auto-generates behavioral + technical interview questions.  |
| 🔜 Resume Scoring & Feedback  | Grade resumes against industry keywords and metrics (planned).             |

---

##  Technologies Used

| Category         | Stack                                                                 |
|------------------|----------------------------------------------------------------------|
| 🐍 Programming    | Python 3.x                                                            |
| 📚 Libraries      | `transformers`, `sentence-transformers`, `nltk`, `spacy`, `sklearn`  |
| 📊 Data Handling  | `pandas`, `numpy`, `matplotlib` (for optional visualizations)         |
| 🧠 NLP Models     | SBERT (`all-MiniLM-L6-v2`), TF-IDF                                     |
| 🔬 Deployment     | Jupyter Notebook / Google Colab                                      |

---

##  Methodology

1. **Input**:
    - Resume (as plain text or preformatted string)
    - One or more Job Descriptions (JD)

2. **Text Preprocessing**:
    - Clean, tokenize, lowercase, remove stopwords
    - Lemmatization using spaCy or NLTK

3. **Embedding Generation**:
    - TF-IDF vectorizer (Scikit-learn)
    - BERT-based embeddings using `sentence-transformers`

4. **Similarity Computation**:
    - Cosine Similarity between resume vector and JD vectors
    - Ranking based on similarity scores

5. **Output**:
    - Ranked list of JDs by match score
    - (Planned) Suggested topics/questions for interview prep

---

##  Example

### ✅ Sample Resume:
Experienced data analyst skilled in Python, SQL, and Tableau. Previously worked with forecasting models and business intelligence dashboards.
### ✅ Sample Resume:
Looking for a data analyst with expertise in SQL, business dashboards, and statistical forecasting models. Python skills preferred.

Match Score (TF-IDF): 0.73
Match Score (BERT):   0.89

Ranked JD:
1. Data Analyst (0.89)
2. Junior BI Analyst (0.78)
3. Machine Learning Intern (0.62)



