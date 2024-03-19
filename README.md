# Ex02 Django ORM Web Application
## Date:18.03.2024

## AIM
To develop a Django application to store and retrieve data from a Railway database using Object Relational Mapping(ORM).  

## Entity Relationship Diagram
![WhatsApp Image 2024-03-19 at 10 08 13_d0513fd0](https://github.com/MangariDeeraj/ORM/assets/149365485/14e564ad-571c-4be4-b0ae-7d3906ef0406)


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

```
models.py

from django.db import models
from django.contrib import admin
class Train(models.Model):
    Train_code=models.CharField(max_length=20,primary_key=True)
    Train_name=models.CharField(max_length=100)
    start_time=models.DateTimeField()
    End_time=models.DateTimeField()
    start_station_code=models.CharField(max_length=20)
    End_station_code=models.CharField(max_length=20)
 
class TrainAdmin(admin.ModelAdmin):
    list_display=('Train_code','Train_name','start_time','End_time','start_station_code','End_station_code')

admin.py


from django.contrib import admin

from .models import Train, TrainAdmin

admin.site.register(Train, TrainAdmin)

```


## OUTPUT
![Screenshot 2024-03-18 210034](https://github.com/MangariDeeraj/ORM/assets/149365485/c184ba26-cd58-45d0-a9ae-f08e02c6da99)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
