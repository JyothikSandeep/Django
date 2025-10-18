# Django

Creating a virtual environment -

why to create a virtual environment??

```python
python -m venv myworld
 
```

We need to activate the virtual environment using the command 

```python
myworld\Scripts\activate

```
Djjango installation

```
(myworld) ... $ python -m pip install Django

```

Create a Django project

```python
django-admin startproject myapp

# to enter into the path
cd myapp
```


Start the project:


Command to start the project

```python

python manage.py runserver

```

creating a Django app:

```python
python manage.py startapp hello
```

Create Admin:

```python
python manage.py createsuperuser
```
-it will ask for a username and then the password. When you type the password you will not be able to see it. you can then use the username and password to login to the admin panel



Database commands:

create commands:

# 1. Create and save
s = Student(name="John", age=20, course="Python")
s.save()

# 2. Or directly create
Student.objects.create(name="Jane", age=22, course="Django")


# read commands

# Get all records
Student.objects.all()

# Get one record by id
Student.objects.get(id=1)

# Filter records
Student.objects.filter(age=20)

# Exclude records
Student.objects.exclude(age=20)

# Get first / last record
Student.objects.first()
Student.objects.last()

# Order by field
Student.objects.order_by('age')        # ascending
Student.objects.order_by('-age')       # descending

# Count records
Student.objects.count()


# update commands

# Get the record
s = Student.objects.get(id=1)

# Change fields
s.age = 25
s.course = "Django Advanced"

# Save changes
s.save()

# Or update multiple records at once
Student.objects.filter(age=20).update(course="Updated Course")

# deletion command

# Delete one record
s = Student.objects.get(id=1)
s.delete()

# Delete multiple records
Student.objects.filter(age=25).delete()

# Delete all records ( careful!)
Student.objects.all().delete()


