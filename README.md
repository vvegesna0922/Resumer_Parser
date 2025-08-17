This Project is a Resume Parser. 


The outline for the project:

resume-job-matcher/
│── data/
│   ├── resumes/                # Example resumes (txt, pdf, or json format)
│   ├── job_descriptions/       # Sample job descriptions
│   └── processed/              # Preprocessed embeddings and tokenized files
│
│── notebooks/
│   ├── 01_data_preprocessing.ipynb   # Convert resumes + JDs into text, clean
│   ├── 02_embedding_experiments.ipynb # Try BERT embeddings, sentence-transformers
│   ├── 03_scoring_models.ipynb        # Train scoring models (cosine, ML, etc.)
│   └── 04_demo_prototype.ipynb        # Interactive prototype demo
│
│── src/
│   ├── __init__.py
│   ├── preprocess.py          # Clean text (remove stopwords, normalize, extract skills)
│   ├── embeddings.py          # Functions for BERT embeddings (HuggingFace, SBERT)
│   ├── similarity.py          # Compute cosine similarity, skill match scoring
│   ├── scoring.py             # Final scoring logic (weighted skills + embeddings)
│   ├── extractor.py           # Extract skills/keywords using NER or regex
│   ├── recommender.py         # Suggest missing skills, courses, extra activities
│   └── utils.py               # Helper functions (logging, configs, pdf-to-text, etc.)
│
│── app/
│   ├── main.py                # FastAPI or Flask backend
│   ├── routes.py              # Endpoints (upload resume, JD, return score)
│   ├── templates/             # Frontend HTML (if Flask)
│   └── static/                # CSS, JS
│
│── tests/
│   ├── test_embeddings.py
│   ├── test_similarity.py
│   └── test_scoring.py
│
│── requirements.txt           # HuggingFace, sentence-transformers, scikit-learn, FastAPI/Flask
│── README.md                  # Project overview, setup instructions
│── config.yaml                # Config file for model paths, thresholds
│── run.py                     # Main entry script
