# when starting a new Django project

add static files to your settings.py

    STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'portfolio/static/')
    ]

    STATIC_ROOT = os.path.join(BASE_DIR, 'static')
    STATIC_URL = '/static/'

    STATICFILES_FINDERS = [
    'django.contrib.staticfiles.finders.FileSystemFinder',
    'django.contrib.staticfiles.finders.AppDirectmoriesFinder',
    ]

    MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
    MEDIA_URL = '/media/'


register your app in the settings AND with the admin.py file.  Under your app/admin.py file you should have something like the following:

    from django.contrib import admin
    from .models import Goal

    admin.site.register(Goal)


Change the backend to postgreSQL ???

### Models.py

when setting fields in models.py
  - null=True tells the database to allow Null value types
  - blank=True tells the form/admin that this field is optional


---
[Django](https://ch3ck3rs.github.io/knowledge_base/Django)

[Home](https://ch3ck3rs.github.io/knowledge_base)
