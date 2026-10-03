# Baisan Elementary School website

A Django school homepage for Baisan Elementary School in Bayawan City, Negros Oriental.

## Run locally

```powershell
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Open http://127.0.0.1:8000/.

## Deploy to Render

The included `render.yaml` creates a free Render web service. Connect the GitHub repository to Render as a Blueprint and apply the configuration. Render generates the production secret key, while `build.sh` installs dependencies, runs migrations, and collects static files.

This starter uses SQLite and has no database-backed school content. Render's free web service has an ephemeral filesystem, so database changes and uploaded files do not persist across deploys or restarts. Add a persistent database before storing announcements, inquiries, or other important data.

The homepage is in `templates/school/home.html`; styles, scripts, and images are in `static/`.
