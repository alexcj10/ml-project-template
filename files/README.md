# mlsetup

One command ML project scaffolding CLI. Works on Windows, Mac, and Linux.

## Install

```bash
pip install mlsetup
```

## Usage

```bash
mlsetup init project_name
```

That single command will:

- Create the project folder
- Create all directories — `data`, `src`, `notebooks`, `configs`, `logs`, `tests`
- Create all required files — `.gitignore`, `.env`, `config.yaml`, `train.py`, `eda.ipynb`
- Create and configure a virtual environment inside `.venv`
- Upgrade `pip`, `setuptools`, `wheel`
- Install common ML dependencies — `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `jupyter`, `mlflow`, `fastapi`, `uvicorn`, `python-dotenv`
- Save `requirements.txt`
- Generate a `README.md`
- Initialize a Git repository with an initial commit

## Project Structure Created

```
project_name/
├── .venv/                 Virtual environment (auto-generated, never touch)
├── data/
│   ├── raw/               Original, untouched data.
│   └── processed/         Cleaned and transformed data.
├── notebooks/
│   └── eda.ipynb          Exploration and visualization only.
├── src/
│   ├── features/          Feature engineering logic.
│   ├── models/            Model definition.
│   ├── training/
│   │   └── train.py       Main training entry point.
│   └── inference/         Prediction and serving logic.
├── configs/
│   └── config.yaml        All settings and hyperparameters.
├── logs/                  Training logs.
├── tests/                 Unit and integration tests.
├── .env                   Secret keys. Never commit.
├── .gitignore
├── requirements.txt
└── README.md
```

## After Setup

```bash
cd project_name

# Mac / Linux
source .venv/bin/activate

# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Run training
python src/training/train.py
```

## Other Commands

```bash
mlsetup --help       Show help
mlsetup --version    Show version
```

## Requirements

- Python 3.8 or higher
- Git (optional, for auto git init)

## License

MIT
