# Ex02 Django ORM Web Application
# Date: 6-12-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM

```
1.models.py

from django.db import models

from django.contrib import admin

class Bank_Loan(models.Model):

    loan_id = models.CharField(max_length=20,primary_key=True)

    loan_type = models.CharField(max_length=30)

    loan_amd = models.FloatField()

    cust_acno = models.IntegerField()

    cust_name = models.CharField(max_length=50)


class Bank_LoanAdmin(admin.ModelAdmin):

    list_display = ('loan_id', 'loan_type','loan_amd','cust_acno','cust_name')

2.admin.py

from django.contrib import admin

from.models import Bank_Loan, Bank_LoanAdmin


admin.site.register( Bank_Loan,Bank_LoanAdmin)
```
# OUTPUT
![alt text](image.png)

![alt text](image-1.png)
# RESULT
Thus the program for creating a database using ORM hass been executed successfully
