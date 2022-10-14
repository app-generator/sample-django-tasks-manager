# [Django Tasks Manager](https://github.com/app-generator/django-tasks-manager) - `How to use it`

This repository provides a `step-by-step` integration of [Django Tasks Manager](https://github.com/app-generator/django-tasks-manager), an open-source [Python Library](https://pypi.org/project/django-tasks-manager/) built on top of `Celery`. In the end, the `superusers` are able to manage tasks (create, revoke) and visualize the output and runtime logs - The product is actively supported by [AppSeed](https://appseed.us/).

> Features 

- ✅ Create/Revoke Celery Tasks
- ✅ View LOGS & Output
- ✅ Minimal Configuration
- ✅ Installation via PyPi
- ✅ Available [TASKS](https://github.com/app-generator/django-tasks-manager/blob/main/django_tm/tasks.py) (provided as starting samples)
  - `users_in_db()` - List all registered users
  - `execute_script()` - let users execute the [scripts](https://github.com/app-generator/django-tasks-manager/tree/main/django_tm/celery_scripts) defined in `CELERY_SCRIPTS_DIR` (configuration parameter)

<br />

![Django Tasks Manager - Sample](https://user-images.githubusercontent.com/51070104/195776227-11a6a8a7-6481-4113-9d0f-95eae7b2faea.jpg)

<br />

## 👉 Project Creation - `v0.0.1` tag

In this phase only the basic files are provided: 

- `README.md`
- `CHANGELOG.md`
- `.gitignore` 

Besides the files, the Virtual environment is created: 

```bash
$ python3 -m venv env        # create virtual environment 
$ source env/bin/activate    # actvate the VENV 
$ pip install --upgrade pip  # update PIP
```

<br />

## 👉 Create the Django Project - `v0.0.2` tag

In this phase, the usual commands are used: 

```bash
$ pip install Django                # Install Django  
$ django-admin startproject core .  # create 'core' project 
$ python manage.py migrate          # migrate DB
$ python manage.py runserver        # Access the basic app in the browser
```

<br />

## 👉 Install Django TM Package - `v0.0.3` tag

The new is installed and the related directories are created: 

```bash
$ pip install django-tasks-manager  # install the package 
$ mkdir celery_logs                 # here the logs are saved
$ mkdir celery_scripts              # scripts to be executed 
```

The sample scripts are provided by the package for a fast start: 
https://github.com/app-generator/django-tasks-manager/tree/main/django_tm/celery_scripts

<br />

## 👉 Install Django TM Package - `v0.0.4` tag

Update configuration and routing. Here are the impacted files:

- `core/settings.py`
- `core/urls.py`

<br />

## 👉 Final set up & Usage  - `v1.0.0` tag

In this phase the project becomes usable. The database is migrated and a superuser is created to access and manage the tasks. 

```bash
$ python manage.py makemigrations      # generate the new SQL
$ python manage.py migrate             # migrate (update) DB
$
$ python manage.py createsuperuser     # create the app user
$
$ # Start the application 
$ python manage.py runserver           
```

> Note: The `celery` task manager should be started using a different terminal

```bash
$ celery --app=django_tm.celery.app worker --loglevel=info
```

Once the superuser is authenticated, the tasks manager should be usable: 

> `http://127.0.0.1:8000/tasks` 

<br />

![Django Tasks Manager - Tasks View Log.](https://user-images.githubusercontent.com/51070104/195777287-7484e731-f4ff-4465-9d3b-78517ee52658.jpg)

<br />

![Django Tasks Manager - View ALL Tasks.](https://user-images.githubusercontent.com/51070104/195777318-e2e7891c-4863-4fd1-9ee5-aba8ac00d418.jpg)

<br />

![Django Tasks Manager - View tasks in admin section.](https://user-images.githubusercontent.com/51070104/195777525-c4773ea7-4e71-4ed0-99f3-8f864243e894.jpg)

<br />

---
[Django Tasks Manager](https://github.com/app-generator/django-tasks-manager) - Free sample provided by [AppSeed](https://appseed.us)
