release: python manage.py migrate
web: gunicorn hrms_project.wsgi:application --bind 0.0.0.0:$PORT
