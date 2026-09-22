# WeWork Executive Portfolio Advisor

A Streamlit classroom proof of concept for exploring a supplied WeWork portfolio hierarchy by region, market, and location, with optional AI chat about the selected portfolio scope.

Operational and financial metrics are simulated once per session. This application does not provide live WeWork business data.

## Run locally

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m streamlit run app.py
```

The dashboard works without an API key. To enable AI chat, create `api_secrets.py` beside `app.py`:

```python
OPENAI_API_KEY = "your-api-key"
```

Replace the placeholder with your own key and restart the app. This file is excluded from Git. AI chat sends the selected portfolio data and conversation history to the OpenAI API and requires API access.

## Project files

- `app.py`: dashboard, simulated metrics, scope filters, and AI advisor.
- `portfolio.py`: supplied portfolio hierarchy.
- `UI MockUp.png`: UI reference image.
- `requirements.txt`: direct dependency versions from the local environment.
