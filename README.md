# exp3 — Python CI Docker Lab

This folder contains a tiny Python project for a CI pipeline demo:

- `app.py` — small `add(a, b)` function and a CLI print
- `tests/test_app.py` — `pytest` tests
- `Dockerfile` — builds a minimal image that runs `python app.py`

Quick local steps:

```powershell
cd exp3
python -m pip install --upgrade pip
pip install -r requirements.txt
pytest -q
docker build -t exp3-app:latest .
```

To add CI: copy `.github/workflows/ci-dockerhub.yml` and configure Docker Hub secrets.
