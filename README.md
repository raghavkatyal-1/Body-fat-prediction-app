# Body Fat Prediction App

Predict your body fat percentage from simple inputs — fast, offline, and easy to use.

This repository contains a compact body-fat predictor trained and packaged for quick experimentation. Use the provided `app.py` for a quick prediction interface, or open `body-fat-predictor.ipynb` to explore the data and retrain the model.

---

## Key features

- Lightweight body-fat prediction model stored in `model/`
- Notebook-driven EDA and training in `body-fat-predictor.ipynb`
- Simple runnable script `app.py` for quick predictions or local serving
- Minimal dependencies (see `requirements.txt`)

## Quick demo

1. Install dependencies:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. Run the app (assumes `app.py` exposes a CLI or simple local server):

```bash
python app.py
# or, if app.py starts a local Flask/FastAPI server, open http://localhost:5000 (or the printed URL)
```

3. Open `body-fat-predictor.ipynb` to inspect the dataset, model training, and evaluation steps.

> Note: If `app.py` expects specific command-line arguments or a different run command, check the file header for usage details.

## Installation

- Clone the repository:

```bash
git clone https://github.com/raghavkatyal-1/Body-fat-prediction-app.git
cd Body-fat-prediction-app
```

- Create and activate a virtual environment, then install dependencies:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

There are two primary ways to use this project:

1. Interactive notebook

   - Open `body-fat-predictor.ipynb` in Jupyter / VS Code.
   - The notebook contains data exploration, preprocessing, model training, and evaluation code.

2. Script / app

   - `app.py` provides a minimal interface to load the model from `model/` and make predictions.
   - Typical usage examples (depending on how `app.py` is implemented):

```bash
python app.py --help
python app.py --input "age=30,height=170,weight=70,neck=38,waist=80,hip=95"
```

Adjust the input format according to the script's expected arguments. If the project instead exposes an HTTP API, send a POST request to the prediction endpoint with the required fields.

## Model

- The trained model artifacts are located in the `model/` directory.
- The notebook includes the training pipeline and the code that produced the model. You can retrain with new data or tweak preprocessing and hyperparameters from the notebook.

### Quick retrain

1. Open `body-fat-predictor.ipynb`.
2. Re-run the training cells after making any changes to preprocessing or model configuration.
3. Save/export the new model into `model/` so `app.py` can pick it up.

## Project structure

```
├── app.py                       # Small script / server to run predictions
├── body-fat-predictor.ipynb     # Notebook with EDA and model training
├── model/                       # Trained model artifacts
├── requirements.txt             # Python dependencies
└── README.md                    # This file
```

## Assumptions

- `app.py` offers either a CLI or a local server to load the model in `model/` and perform predictions.
- The notebook contains the full training and preprocessing pipeline. If your setup differs, adjust the commands above accordingly.

If these assumptions are incorrect for your repo, tell me which behavior you expect (CLI vs API) and I can update this README with exact commands.

## Contributing

Contributions are welcome:

1. Open an issue describing the bug or feature.
2. Create a branch, add tests or notebook examples where relevant, and open a PR.

Please follow these guidelines:

- Keep code style consistent with the repository.
- Add a short description in PRs about what changed and why.

## License

This project currently does not contain a LICENSE file. Add a license (e.g., MIT) if you intend to make the project open-source.

## Contact

For questions or help, open an issue in the repository or reach out to the repository owner.

---

Happy experimenting — build, evaluate, and iterate on body composition predictions with this lightweight starter!
