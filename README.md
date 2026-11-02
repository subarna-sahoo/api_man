# api_man

A Django project scaffold for an API service, with two apps (`api_client` and `user`) created but not yet built out.

> **Status:** scaffold only. Models, views and URLs are still empty; only the Django admin is wired up.

## Running

```bash
python -m venv venv && source venv/bin/activate
pip install django
python manage.py migrate
python manage.py runserver     # admin at http://localhost:8000/admin/
```

## Structure

```
core/          Project settings and URLs
api_client/    App for API client management (empty)
user/          App for users (empty)
```

## Configuration

Secrets are read from **environment variables**, so nothing sensitive lives in the code. Copy [`.env.example`](.env.example) to `.env` (it is git-ignored) or export the variables in your shell:

| Variable | Purpose |
|---|---|
| `DJANGO_SECRET_KEY` | Django `SECRET_KEY`. If unset, a random key is generated at startup (fine for local dev). |

The same values are stored as **GitHub Actions secrets** on this repo (*Settings → Secrets and variables → Actions*), so CI/CD workflows can use them as `${{ secrets.NAME }}`.

## License

MIT. See [LICENSE](LICENSE).
