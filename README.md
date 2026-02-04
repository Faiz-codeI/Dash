# IDX Dashboard (Streamlit)

## Local Setup
1) Create venv:
```
python -m venv .venv
```
2) Activate:
- Windows PowerShell:
```
.\.venv\Scripts\Activate.ps1
```
- Bash:
```
source .venv/bin/activate
```
3) Install deps:
```
pip install -r requirements.txt
```

## Run Locally
```
streamlit run app.py
```

## Folder Structure
- `app.py`: Streamlit entry point
- `src/`: dataio, technical, scoring, insights
- `data/`: input datasets (sectors/*.xlsx, fundamentals_table.csv, universe_tickers.txt)
- `.streamlit/config.toml`: Streamlit config
- `scripts/`: local run helpers

## Deploy to Render
1) Push repo to GitHub
2) Render > New > Web Service (or New Blueprint Instance if using render.yaml)
3) Build command:
```
pip install -r requirements.txt
```
4) Start command:
```
streamlit run app.py --server.port $PORT --server.address 0.0.0.0
```
5) Environment variables (optional):
- `DATA_DIR` if you want to override data path
