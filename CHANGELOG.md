# Change Log

## [1.0.0] 2022-10-14
### Stable USE

- Complete the set up 
- Start and use the app 

## [0.0.4] 2022-10-14
### Improvements

- Added configuration:
  - Update routes in `core/urls.py`
  - Update `core/settings.py`
    - import `os` package, used in BASE_DIR definition
    - Update `INSTALLED_APPS`
    - Include the new templates, `TEMPLATES` section
    - Added `Django & Celery` (end of the file)

## [0.0.3] 2022-10-14
### Improvements

- Install [django-tasks-manager](https://github.com/app-generator/django-tasks-manager) via `PIP`
- Create directories:
  - `celery_logs` - for tasks logging
  - `celery_scrips` - with [sample scripts](https://github.com/app-generator/django-tasks-manager/tree/main/django_tm/celery_scripts)
    - check-db-health.py, check-disk-free.py, clean-database.py

## [0.0.2] 2022-10-14
### Improvements

- Added the minimal Django project

## [0.0.1] 2022-10-14
### Project Creation 

- The start of the project is tracked
  - just the minimal structure
