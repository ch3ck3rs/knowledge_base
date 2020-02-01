# when starting a new Django project

add static files to your settings.py

    STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'portfolio/static/')
    ]

    STATIC_ROOT = os.path.join(BASE_DIR, 'static')
    STATIC_URL = '/static/'

    STATICFILES_FINDERS = [
    'django.contrib.staticfiles.finders.FileSystemFinder',
    'django.contrib.staticfiles.finders.AppDirectoriesFinder',
    ]

    MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
    MEDIA_URL = '/media/'


register your app in the settings AND with the admin.  Under your app/admin.py
file you should have something like the following:

    from django.contrib import admin

    # Register your models here.
    from .models import Goal

    admin.site.register(Goal)



---
[Django](https://ch3ck3rs.github.io/knowledge_base/python/django)

[Python](https://ch3ck3rs.github.io/knowledge_base/python)

[Home](https://ch3ck3rs.github.io/knowledge_base)
