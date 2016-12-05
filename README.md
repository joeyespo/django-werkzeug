Django Werkzeug
===============

[![Current version on PyPI](http://img.shields.io/pypi/v/django-werkzeug.svg)][pypi]

Enhances Django `runserver` with [Werkzeug][].

This project uses [Django Extensions][] under the hood. It "wraps" it, along
with Werkzeug, so you don't have to add an explicit `werkzeug` dependency
to your `requirements.txt` or remember a new command.


Why
---

Werkzeug and its builtin error page has proven to be indispensable in a number
of Django projects. While Django Extensions is also a great tool, the full
extent of it is not always needed in specific projects.

Also, when committing to Werkzeug, it's convenient to run the `runserver`
instead of learning a new command. This brings newcomers to your team up to
speed without further instruction and doesn't require existing members to
change their muscle memory during their day-to-day.

If you want to use Werkzeug on certain projects, but don't want to keep track
of which ones, this package is for you.


Requirements
------------

Django Werkzeug requires Django 1.8 or later.


Installation
------------

```bash
$ pip install django-werkzeug
```

Then enable it by adding it to `INSTALLED_APPS` in your `settings.py` file:

```python
INSTALLED_APPS = [
    'django_werkzeug',
    ...
]
```


Usage
-----

```bash
$ python manage.py runserver
```

Or to run Django's classic builtin server, run:

```bash
$ python manage.py runserver_classic
```


Contributing
------------

1. Check the open issues or open a new issue to start a discussion around
   your feature idea or the bug you found
2. Fork the repository and make your changes
3. Create a new pull request


[pypi]: http://pypi.python.org/pypi/django-werkzeug/
[werkzeug]: https://github.com/pallets/werkzeug
[django extensions]: https://github.com/django-extensions/django-extensions
