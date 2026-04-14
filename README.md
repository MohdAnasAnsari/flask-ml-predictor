# Flask ML Predictor

## Overview
This project demonstrates a minimal end-to-end machine learning workflow:
1. Train a simple logistic regression model in a Jupyter notebook.
2. Serialize the trained model to disk.
3. Serve predictions through a Flask web app with a basic HTML form.

It is intentionally small and easy to understand, making it a good learning example for ML deployment basics.

## What It Does
- Uses a toy dataset with `Age` and `Fare` as inputs.
- Predicts a binary outcome labeled `Survived` (0 or 1).
- Provides a web form to enter inputs and returns a JSON prediction.

## Project Structure
- `Untitled.ipynb` — model training notebook.
- `model.pkl` — serialized trained model.
- `app.py` — Flask application that loads the model and serves predictions.
- `templates/index.html` — simple UI for user input.
- `requirements.txt` — dependencies.
- `procfile` — gunicorn startup command for deployment platforms.

## Run Locally
1. Create and activate a virtual environment (optional but recommended).
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Start the Flask app:

```bash
python app.py
```

4. Open your browser at:
```
http://127.0.0.1:5000
```

## API Usage
`POST /predict` accepts form fields:
- `age` (float)
- `fare` (float)

Example response:
```json
{"Survived": 1}
```

## Notes
- The dataset is tiny and hard-coded for demo purposes.
- Accuracy shown in the notebook is not meaningful for real-world use.
- This is meant as a deployment example, not a production ML model.

## License
MIT
