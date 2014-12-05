#Basic Flask Tutorial

This tutorial covers creating a basic Flask application using Python 3.4. [Flask](http://flask.pocoo.org/) is a micro-framework for Python that lets you easily build web applications.

###Installing Python 3.4

If you need to install python 3.4 then go to this website https://www.python.org/downloads/ and follow the instructions.

###Installing Flask Using Pip

[Pip](https://pypi.python.org/pypi/pip) is a package manager for Python, and it comes pre-installed with Python 3.4. You can use Pip to install Flask with the following command:

```shell
  pip3 install flask
```

###Writing your first Flask application

Create a folder for your application. Let's call it Flask-App. On linux:

```shell
  mkdir Flask-App
```

Now let's create a python file in that directory:

```shell
  cd Flask-App
  touch flask-app.py
```

We will create our Flask app in flask-app.py. Within flask-app.py we need to import the Flask package, which we do with this line of code

```python
  from flask import Flask
```


Write Hello World

Explain each line.


Run App

python basic-flask-app.py. Explain hitting it via browser.


Setting debug to reload flask app on change to code.

app.run(debug=True)
