# Spotify Hybrid Recommendation System

## About
A hybrid machine learning recommendation engine designed to improve **USER ENGAGEMENT** and **USER RETENTION** for subscription-based Spotify users. The Hybrid system (Using Weights) combines **Content-Based Filtering** and **Collaborative Filtering** to deliver both personalized and diverse song recommendations.

Users interact with the system through a **Streamlit web application**, where they input a song name and artist name to receive recommended songs.

Repository: https://github.com/constantaryan/Spotify-Hybrid-Recommendation-System

---

## Table of Contents
- About
- Features
- Tech Stack
- Installation
- Usage
- Project Structure
- Architecture Overview
- Environment Variables
- Testing
- Contributing
- License

---

## Features

### Content-Based Filtering
Analyzes song audio features and metadata to recommend songs similar to the user's input.

### Collaborative Filtering
Learns from listening patterns across multiple users to suggest songs others with similar taste enjoy.

### Hybrid Recommendation Engine
Combines content and collaborative filtering to balance **personalization** and **diversity**, helping avoid the cold-start problem.

### Streamlit Web Interface
Users simply enter:
- Song Name
- Artist Name

The application then returns a list of recommended tracks and the Preview of the song.

---

## Tech Stack

Language
- Python

Frontend
- Streamlit

Machine Learning
- Pandas
- NumPy
- Scikit-learn
- Dask

Development Environment
- Jupyter Notebook
- VS Code

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/constantaryan/Spotify-Hybrid-Recommendation-System.git
cd Spotify-Hybrid-Recommendation-System
```

### Create Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Usage

Run the Streamlit application:

```bash
streamlit run app.py
```

Open your browser and go to:

```
http://localhost:8000
```

Enter a **song name** and **artist name** to receive recommended songs.

---

## Project Structure

```
Spotify-Hybrid-Recommendation-System
├── data
│  ├── .gitignore
│  ├── cleaned_data.csv
│  ├── collab_filtered_data.csv
│  ├── interaction_matrix.npz
│  ├── Music Info.csv
│  ├── Music Info.csv.dvc
│  ├── track_ids.npy
│  ├── transformed_data.npz
│  ├── transformed_hybrid_data.npz
│  ├── User Listening History.csv
│  └── User Listening History.csv.dvc
├── deploy
│  └── scripts
│     ├── install_dependencies.sh
│     └── start_docker.sh
├── notebooks
├── __pycache__
│  ├── content_based_filtering.cpython-311.pyc
│  ├── data_cleaning.cpython-311.pyc
│  └── hybrid_recommendations.cpython-311.pyc
├── .dvcignore
├── .gitignore
├── app.py
├── appspec.yml
├── collaborative_filtering.py
├── content_based_filtering.py
├── data_cleaning.py
├── Dockerfile
├── dvc.lock
├── dvc.yaml
├── hybrid_recommendations.py
├── README.md
├── requirements.txt
├── test_app.py
├── transformer.joblib
└── transform_filtered_data.py
```

---

## Architecture Overview

### Data Processing
- Cleaning Spotify dataset
- Handling missing values
- Feature scaling

### Content-Based Model
- Uses cosine similarity between audio features

### Collaborative Filtering Model
- Learns user-song interaction patterns

### Hybrid Recommendation Layer
Combines both models to generate the final recommendation list.

### Frontend
Streamlit interface for user input and displaying recommendations.

---


## Testing

If tests are added:

```bash
pytest tests/
```

---

## Contributing

Contributions are welcome.

Steps:

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/new-feature
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push the branch

```bash
git push origin feature/new-feature
```

5. Open a Pull Request

---


