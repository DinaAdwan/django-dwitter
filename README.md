# Dwitter — Django social network

A small Twitter-style social network built with Django during the Gaza Sky Geeks backend programme.

## Features
- Every new user gets a profile automatically (created with a `post_save` signal)
- Follow and unfollow other users (self-referencing many-to-many relationship)
- Post short messages ("dweets", max 140 characters)
- Dashboard feed showing dweets from the people you follow, newest first

## Tech
Python · Django 4.1 · SQLite · Django templates

## Run locally
```bash
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```
Log in through `/admin/` first, then open `/`.

The secret key is read from the `DJANGO_SECRET_KEY` environment variable; a development fallback is used if it isn't set.
