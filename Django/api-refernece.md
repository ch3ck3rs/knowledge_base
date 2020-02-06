all the places you must edit to create an api.  view the [Django-restframework quickstart guide](https://www.django-rest-framework.org/tutorial/quickstart/) to get more details.  This is just a log.

1. add 'rest_framework' under INSTALLED_APPS in the settings.py
2. create class AppSeralizer in serializers.py
3. add class AppViewSet to views.py
4. in project/urls.py import router from rest_framework
