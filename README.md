# Ex02 Django ORM Web Application
## Date: 05-03-24

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Diagram](https://github.com/gowthamsec/ORM/assets/147933945/329f2b50-d14b-473e-9d77-9db6c3348f0c)
## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
-Models
```
from django.db import models
from django.contrib import admin
class Books_DB(models.Model):
    serial=models.IntegerField(primary_key=True);
    title=models.CharField(max_length=20);
    author=models.CharField(max_length=20);
    price=models.IntegerField( );
    genre=models.CharField(max_length=20);
class Books_DBAdmin(admin.ModelAdmin):
    list_display=("serial","title","author","price","genre");
```
-Admin
```
from django.contrib import admin
from .models import Books_DB,Books_DBAdmin 
admin.site.register(Books_DB,Books_DBAdmin)
```
## OUTPUT
![output](https://github.com/gowthamsec/ORM/assets/147933945/72c8380d-2118-4de6-84c7-a4906cb1e7ea)
## RESULT
Thus the program for creating a database using ORM hass been executed successfully
