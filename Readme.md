# django hello world

# Tags
`Django` `Django Hello world` `my first applicaiton`

## Help

***
```
python -m virtualenv myenv
myenv\scripts\activate.bat
pip install -r requiremets.txt
```
***
```
django-admin startproject [project-name] .
python manage.py startapp [app-name]
```
***
```
project > settings.py >

INSTALLED_APPS = [
  .
  .
  .
  [app-name]
]
```
***
```
project > urls.py >

from django.contrib import admin
from django.urls import path,include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('home.urls')),
]
```
***
```
app > urls.py >

from django.urls import path
from home import views

urlpatterns = [
    path('', views.index),
]
```
***
```
app > views.py

from django.http.response import HttpResponse

def index(request):
    return HttpResponse('Hello world')
```
***
```
python manage.py makemigrations home
python manage.py migrate
python manage.py runserver
```