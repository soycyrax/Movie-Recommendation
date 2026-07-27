# Movie Recommendation

A small Flask web app that recommends movies from `movies.csv` based on genre ratings entered by the user.

## Requirements

- Python 3.10.6 was used to create and test the local virtual environment.
- Windows PowerShell commands are shown below.

Exact Python package versions are pinned in `requirements.txt`:

```text
Babel==2.18.0
blinker==1.9.0
click==8.4.2
colorama==0.4.6
Flask==2.2.5
Flask-Babel==4.0.0
Flask-Table==0.5.0
itsdangerous==2.2.0
Jinja2==3.1.6
MarkupSafe==3.0.3
numpy==2.2.6
pandas==2.3.3
python-dateutil==2.9.0.post0
pytz==2026.3.post1
six==1.17.0
tzdata==2026.3
Werkzeug==2.2.3
```

`Flask==2.2.5` and `Werkzeug==2.2.3` are intentional. `Flask-Table==0.5.0` is an older package and is not compatible with newer Flask 3.x releases.

## Setup

From the project folder:

```powershell
cd "D:\Office\Projects\Movie Recommendation\Code"
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell blocks virtual environment activation, run this once in the same terminal:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
.\.venv\Scripts\Activate.ps1
```

## Run

With the virtual environment activated:

```powershell
python .\Movie_Recommender.py
```

Or run directly through the virtual environment without activating:

```powershell
.\.venv\Scripts\python.exe .\Movie_Recommender.py
```

Open the app at:

```text
http://127.0.0.1:5000
```

Stop the server with `Ctrl+C` in the terminal.

## Project Structure

```text
Movie_Recommender.py   Flask application entry point
movies.csv             Movie dataset used by the recommender
templates/             HTML templates for the Flask views
requirements.txt       Exact dependency versions
```

## Notes

- Keep `movies.csv` in the same folder as `Movie_Recommender.py`; the app reads it using a relative path.
- Do not commit `.venv`, `__pycache__`, or `.pyc` files. They are ignored by `.gitignore`.
