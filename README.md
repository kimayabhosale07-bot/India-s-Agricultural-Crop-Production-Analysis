# Agricultural Production Insights

A Flask website presenting an agricultural production dashboard and a separate agricultural yield story, both embedded from Tableau Public.

## Requirements

- Python 3.10 or newer
- Vercel CLI for deployment (Node.js and npm are required)

## Run locally

From the project root in PowerShell:

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python app.py
```

Open <http://127.0.0.1:5000> in your browser. The homepage is rendered by `templates/agriculture.html`; Flask serves project assets under `/assets`.

## Tableau content

The page embeds the agricultural production dashboard and yield story from Tableau Public. The **Story** button scrolls to the story further down the page. Both visualizations are hosted by Tableau, so an internet connection is required for them to load.

## Deploy to Vercel

This project is configured as a Flask app for Vercel. Sign in to Vercel once from the project directory, then deploy production changes with:

```powershell
npx vercel login
npx vercel --prod
```

Current production deployment: <https://arsha-eight-red.vercel.app>

The project is deployed from the Vercel CLI; automatic deployments from Git pushes are not configured.

## Project layout

- `app.py` - Flask application and homepage route
- `templates/agriculture.html` - agricultural dashboard and story page
- `templates/index.html` - Arsha template page
- `static/` - CSS, JavaScript, images, and vendor assets
- `requirements.txt` - Python dependencies
- `.gitignore` - excludes Python caches, virtual environments, secrets, and Vercel project metadata

`Readme.txt` contains the original Arsha template attribution and license information.
