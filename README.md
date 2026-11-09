# Trivia API

> A full-stack trivia game: a Flask + SQLAlchemy REST API with a React frontend. You can browse, add, delete and search questions, and play quizzes by category.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)

## API endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| GET | `/categories` | List all categories |
| POST | `/categories` | Create a category |
| DELETE | `/categories/<id>` | Delete a category |
| GET | `/questions?page=<n>` | Paginated questions (10 per page) with categories |
| POST | `/questions` | Create a question, or search when `searchTerm` is sent |
| DELETE | `/questions/<id>` | Delete a question |
| GET | `/categories/<id>/questions` | Questions in a category |
| POST | `/quizzes` | Get a random question for the quiz, skipping previous ones |

Errors are returned as JSON with the HTTP status code.

## Project structure

```
backend/    Flask app (flaskr/), models, unit tests (test_flaskr.py), trivia.psql
frontend/   React app that uses the API
```

## Run it

```bash
# backend
cd backend
pip install -r requirements.txt
createdb trivia && psql trivia < trivia.psql
export FLASK_APP=flaskr FLASK_ENV=development
flask run

# frontend (in a second terminal)
cd frontend
npm install
npm start
```

Run the tests with `python test_flaskr.py`. More details are in [backend/README.md](backend/README.md).

## Notes

Built as the API project of the **Udacity Full Stack Web Developer Nanodegree**. The React frontend starter code was provided by Udacity, and the API, endpoints and tests are my implementation.

## Author

**Ahmed Gamal Saber**, Full-Stack Web Developer & AI Engineer
[LinkedIn](https://linkedin.com/in/ahmed-gamal-saber-382081169) · [GitHub](https://github.com/AhmedGamal98)
