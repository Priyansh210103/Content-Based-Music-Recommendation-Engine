# 🎵 LyricMatch: NLP-Powered Song Recommendation Engine

## 📖 Overview
LyricMatch is a **Content-Based Recommender System** that suggests music based on the thematic and emotional "DNA" of song lyrics. Instead of relying on popularity or genre tags, this engine uses **Natural Language Processing (NLP)** to "read" the lyrics of 57,000+ songs and find deep semantic connections between tracks.

---

## 🧠 The Science Behind the Suggestions
The project implements a sophisticated text-processing pipeline to turn human language into mathematical coordinates.

### 1. TF-IDF Vectorization
We use **Term Frequency-Inverse Document Frequency (TF-IDF)** to quantify the importance of words.
* **Term Frequency:** Gives weight to words appearing often in a song.
* **Inverse Document Frequency:** Penalizes common words (like "the," "it," "and") and rewards unique, descriptive words (like "diamond," "revolver," "heartbreak").



### 2. Cosine Similarity Mapping
Once the lyrics are vectorized, every song exists as a point in a high-dimensional space. The engine calculates the **Cosine Similarity** (the angle between vectors) to find matches.
* **Small Angle:** High similarity—the songs share rare, thematic keywords.
* **Large Angle:** Low similarity—the songs have nothing in common lyrically.



---

## 🛠️ Technical Stack
* **Language:** Python 3.10+
* **Data Science:** `Pandas`, `NumPy`
* **Machine Learning:** `Scikit-Learn` (TF-IDF, Pairwise Metrics)
* **Environment:** VS Code

---

## 📊 Key Features
* **Thematic Discovery:** Finds songs with similar "vibes" regardless of genre.
* **Fuzzy Search:** Built-in search functionality that handles partial titles and case-insensitive queries.
* **Scalable Pipeline:** Designed to handle massive text datasets efficiently using sparse matrix math.

---

## 🚀 Example Output
**Search Query:** *"Proud Of You"* **AI Recommendations:**
1. **Be Proud Of Your Man** — Loretta Lynn (Highest thematic overlap)
2. **Jealousy** — Eurythmics
3. **Ain't No Good To Cry** — Allman Brothers Band
4. **Hey Mama** — Kanye West
5. **Don't Give Up** — Peter Gabriel

---

## 📂 Project Structure
* `main.py`: Core logic for vectorization and similarity calculations.
* `spotify_millsongdata.csv`: Dataset containing 57,650 song entries. can be found at "https://www.kaggle.com/datasets/notshrirang/spotify-million-song-dataset?select=spotify_millsongdata.csv"
* `README.md`: Project documentation.
