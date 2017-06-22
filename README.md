Django ORM Standalone Application
=================================

__Author__: masnun@gmail.com


Requirements
------------
This repository doesn't ship with a django installation. The system must have an
existing django installation so that we can safely import required modules. A
django app is absolutely not required. Among other requirements is the db
backend. If you're planning to use mysql or pgsql - please make sure you have
all dependencies met. This code works on Django 1.11.


Application Structure
----------------------
+ __settings.py__ - The Django settings module. Contains the database configuration in it. Modify this file to match your database credentials.
+ __manage.py__ - The famous manage.py script from django projects.
+ __main.py__ - This where we write codes. This is just a sample file to demonstrate how to import models.

+ __data__ - The data directory works as a django application and contains the models.py which is where you put your models according to django conventions

How to setup?
-------------
+ git clone the source as a starting point
+ Change to your project directory
+ Create a new python3 virtualenv: `python3 -m venv .env`
+ Activate the virtualenv: `source .env/bin/activate`
+ Install Django: `pip install django`

How to use?
-----------
+ Generate a new `SECRET_KEY` for your settings.py.
+ Modify settings.py to add your database connection parameters.
+ Open "data/models.py". Modify existing model or add your own.
+ Run `python manage.py makemigrations` to make migration scripts
+ Run `python manage.py migrate` to create the tables and sync db changes. Feel free to use other manage.py commands available for django orm.
+ Every time you make changes to models or change db parameters, don't forget to run the migrations.
