# Class 34 - API Deployment

## What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?

- Keep settings in environment variables.
- Write default values for production configuration.
- Don't hardcode sensitive settings, and don't put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.
- When overriding settings, use the `DJANGO_SETTINGS_MODULE` environment variable.
- Organize settings classes in a `settings` package.
- Use settings only in `settings.py` and manage them as Python code.
- Set the `DJANGO_SETTINGS_MODULE` environment variable explicitly.
- Use only one settings file per Django project.
- Don't put non- Django settings in `settings.py`.
- Provide a `requirements.txt` file.
- Use static files storage for production.
- Use the `check --deploy` command to check deployment settings.
- Configure the logging in production to log to `stdout`.
- Use `django-admin startproject --template` to start a project with a custom settings layout.

## How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

With a couple of lines of config WhiteNoise allows your web app to serve its own static files, making it a self-contained unit that can be deployed anywhere without relying on nginx, Amazon S3 or any other external service. (Especially useful on Heroku, OpenShift and other PaaS providers.)

- Install WhiteNoise with `pip install whitenoise`.
- Add `whitenoise.middleware.WhiteNoiseMiddleware` immediately after the `SecurityMiddleware` (if you are using it) and before all other middleware classes.
- Add `STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'` to `settings.py`.
- Run `python manage.py collectstatic` to collect static files.

## What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?

Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources on a web page to be accessed from another domain outside the domain from which the first resource was served.

You can use the `django-cors-headers` package to configure CORS.

- Install django-cors-headers using pip.
- Add 'corsheaders' to the INSTALLED_APPS setting in settings.py.
- Add 'corsheaders.middleware.CorsMiddleware' to the MIDDLEWARE setting in settings.py.
- Specify the allowed origins using CORS_ORIGIN_ALLOW_ALL or CORS_ORIGIN_WHITELIST in settings.py.
- Optionally, customize other CORS settings like headers, methods, and credentials.
- Restart your Django server.
