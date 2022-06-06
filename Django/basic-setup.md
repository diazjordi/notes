
# PROJECT SETUP

## Create virtual env

```python
python3 -m venv {path to virtual env}
```

## Activate virtual env

--- PowerShell

```PS
<venv>\Scripts\Activate.ps1
```

--- Bash

```bash
source <venv>/bin/activate
```

## Add Django to virtual env 
virtual env must be active

```python
python3 -m pip install Django
```

## Start the Django project

--- creates a sub directory to place Django
project in

```python
django-admin startproject {project name}
```

--- creates Django project in current directory

```python
django-admin startproject {project name} . 
```

Django startproject output setup
```
{project name}/
    manage.py
    {project name}/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

These files are the following:

The outer {project name}/ root directory is a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.

manage.py: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about manage.py in django-admin and manage.py.

The inner {project name}/ directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. {project name}e.urls).

{project name}/__init__.py
: An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read more about packages in the official Python docs.

{project name}/settings.py
: Settings/configuration for this Django project. Django settings will tell you all about how settings work.

{project name}/urls.py
: The URL declarations for this Django project; a “table of contents” of your Django-powered site. You can read more about URLs in URL dispatcher.

{project name}/asgi.py
: An entry-point for ASGI-compatible web servers to serve your project. See How to deploy with ASGI for more details.

{project name}/wsgi.py
: An entry-point for WSGI-compatible web servers to serve your project. See How to deploy with WSGI for more details.

## Run Django Server

```python
python3 manage.py runserver
```
