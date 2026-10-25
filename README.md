# 🎬 CineMatch – Movie Recommendation System using NLP

A content-based movie recommender that runs entirely in the browser. It uses
Natural Language Processing (TF-IDF vectors and cosine similarity) over movie
plots, genres, cast and directors to suggest similar films.

**Live demo:** https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/

## Features

- **Similar to a movie** – type a title (typos are tolerated) and get ranked recommendations.
- **Describe a plot** – type a description such as "astronauts stranded in space" and get matching films.
- **Match score and explanation** – each card shows a similarity percentage and the shared terms behind the match.
- **Genre filter** and adjustable number of results.
- Responsive layout with automatic light and dark mode.
- Single file, no installation, no external libraries.

## How it works

1. **Data:** a catalogue of 36 films (title, year, rating, genres, director, cast, overview).
2. **Text features:** each film's overview, genres, top 3 cast members and director are combined into one document. Person names are merged into single tokens, so "Christopher Nolan" is one term.
3. **NLP preprocessing:** lowercasing, punctuation removal, stop-word removal and light stemming.
4. **Vectorisation:** TF-IDF weighting turns every film into a normalised vector.
5. **Similarity:** cosine similarity ranks all other films against the chosen film (or against the typed description).
6. **Title matching:** exact match, then substring match, then edit-distance (Levenshtein) matching for typos.

## Run locally

Download `index.html` and open it in any modern browser. Nothing else is needed.

## Deploy on GitHub Pages

1. Upload `index.html` and this `README.md` to a repository.
2. Go to **Settings → Pages**.
3. Choose **Deploy from a branch → main → / (root)** and save.

## Project structure

```
├── index.html   # the complete website (HTML, CSS, JavaScript and data)
└── README.md
```

## Tech stack

HTML, CSS, JavaScript (vanilla). NLP implemented from scratch: tokenisation,
TF-IDF and cosine similarity.

## Possible improvements

- Use the full TMDB 5000 dataset with a Python backend (scikit-learn).
- Add semantic recommendations with Sentence-Transformers embeddings.
- Fetch real movie posters through the TMDB API.

## Credits

Movie descriptions in this demo are short original summaries.
