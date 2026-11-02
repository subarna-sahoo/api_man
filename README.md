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

## License

MIT. See [LICENSE](LICENSE).
