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

