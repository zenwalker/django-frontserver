# Django frontserver

Run grunt/gulp watcher and django server with a single command.

## Install

```
$ pip install django-frontserver
```

## Usage

Add `frontserver` to `INSTALLED_APPS` and run:

```sh
$ python manage.py frontserver [--apps=app1,app2] [--nodefault] [--nowatch] [runserver args]
```

This is the same as:

```sh
$ python manage.py runserver
$ gulp default watch
```

Or this if `--apps=blog,shop`:

```sh
$ python manage.py runserver
$ gulp blog blog:watch shop shop:watch
```

## Configuration

```py
FRONTSERVER = {
    'BUILDER': 'gulp', # Command for run
    'BUILDER_ARGS': '', # Additional command-line arguments
    'DEFAULT_TASK': 'default', # Name of default task
    'WATCH_TASK': 'watch', # Name of watch task
}
```
