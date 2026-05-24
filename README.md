# CONTENT-BASED MOVIE RECOMMENDATION SYSTEM
  An end-to-end machine learning project that builds a metadata-driven recommendation engine using Natural language processing(NLP).The system creates a unique textual "DNA" profile for over 4800 films and utilizes geometric vector space modeling to instantly recommend the top 5 closest matching movies to a user's favorite title.

 ## How the system works(The Pipeline):
  The system avoids "blockbluster bias" and the "cold start problem" by analyzing the intrinsic traits of the movie instead of relying on user ratings:
1.Feature Merging: Extracts and clean features from the TMDB 5000 dataset (including plot outlines, genres, structural keywords, director, and top cast members) into a unified string block called `tags`.
2.Token Normalization: Space-strips entity names (e.g., transforming "Johnny Depp" into `johnnydepp`) to isolate unique vector signatures and prevent word collisions.
3.Text Stemming:Utilizes the NLTK `PorterStemmer` to trim words down to their base root forms (e.g., "loving", "liked", and "likes" all resolve to `love`).
4.Vector Quantization: Converts text bodies into numerical coordinates using `CountVectorizer`, creating a 5,000-dimensional sparse array mapping.
5.Similarity Evaluation:Computes spatial proximity between vectors using Cosine Similarity. When a movie is queried, the matrix filters and drops the top 5 closest matching film IDs.

## Tech Stack & Libraries:
1.Language: Python
2.Data Handling:Pandas, NumPy
3.NLP & Text Processing:NLTK (PorterStemmer)
4.Machine Learning:Scikit-Learn (CountVectorizer, Cosine Similarity)
5.Environment:Jupyter Notebook / Anaconda

## Key Business Takeaways:
1.Day-One Utility: Recommends brand-new, zero-interaction movies instantly without waiting for user reviews.
2.Long-Tail Discovery: Maximizes catalog utilization by driving traffic to obscure, highly relevant niche films based purely on content DNA.
