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




---
[Django](https://ch3ck3rs.github.io/knowledge_base/Django)

[Home](https://ch3ck3rs.github.io/knowledge_base)
