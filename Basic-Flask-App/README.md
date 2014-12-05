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

First off, let's create a folder for our application. Let's call it Flask-App. In linux terminal:

```shell
  mkdir Flask-App
```

Now let's create a python file in that directory:

```shell
  cd Flask-App
  touch flask-app.py
```

We will create our Flask app in flask-app.py. Within flask-app.py we need to import the Flask package, which we do with this line of code.

```python
  from flask import Flask
```
This basically means import the class Flask from the python package called flask.

The next thing we need to do is create an instance of the Flask class. We will call this instance 'app' with the following line of code:

```python
  app = Flask(__name__)
```

Therefore, we have:

```python
  from flask import Flask
  app = Flask(__name__)
```

Now 'app' is our Flask object. Using 'app' we can define routes for our web application. A route defines what URLs our web application will respond to. For instance if can create a route /hello then our web application will do something when url localhost:5000/hello is hit. Let's create the /hello route with the following line of code:

```python
  @app.route('/hello')
```

To define what our web application does when that route is hit we need to define a function immediately below that route. Let's define a function called hello that returns the string 'Hello World!':

```python
  def hello():
    return 'Hello World!'
```

Now flask-app.py looks like this:

```python
  from flask import Flask
  app = Flask(__name__)

  @app.route('/hello')
  def hello():
    return 'Hello World!'
```

All that is left to do is to run the app, which we do by adding the following line of code:

```python
  if __name__ == '__main__':
    app.run(host='0.0.0.0', debug=True)
```

The if statement makes sure the application only runs if the script is executed directly from the Python interpreter and not used as an imported module. The app.run actually runs the application.

To start our application we go to our terminal and execute the following command:

```shell
  python3 flask-app.py
```
If successful you should see the following output in the terminal:

```shell
  * Running on http://127.0.0.1:5000/
  * Restarting with reloader
```

Now if we go to a browser and enter  URL http://127.0.0.1:5000/hello, it should come back with 'Hello World!'.
