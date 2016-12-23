# Microbit:Polska website

This repository contains sources of Django application that powers [MicrobitPolska.org](https://www.microbitpolska.org/).

## What's in it?

It's a simple CMS that contains pages and blog posts.

# Contributing to MicrobitPolska website

If you want to contribute to this project just fork it and submit a PR !

Also issues are welcome !

## Setting up a development environment

First, clone the repository:

    git clone https://github.com/MicrobitPolska/microbitpolskaorg.git

Step into newly created `microbitpolskaorg` directory:

    cd microbitpolskaorg

Create a new virtual environment if needed (or use conda env). Then, install all the required dependencies:

    pip install -r requirements.txt

Run the migration to create database schema:

    python manage.py runserver --settings=microbitpolska.local_settings migrate

Create a user so you can login to the admin:

   python manage.py runserver --settings=microbitpolska.local_settings createsuperuser

Run your local server::

    python manage.py runserver --settings=microbitpolska.local_settings


Done!


## Run the tests

We don't have tests yet.


## Static files

To collect the static files:

    python manage.py collectstatic --settings=microbitpolska.local_settings

## Envs

Inside docker/web_app/web_app.env put:

* SECRET_KEY=YOUR_SECRET_KEY
* EMAIL_HOST_USER=YOUR_EMAIL_USER
* EMAIL_HOST_PASSWORD=YOUR_EMAIL_PASSWORD