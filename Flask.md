---
tags: [concept]
---

# Flask
## import flask
```python
from flask import Flask
```

### basic setup
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
	return "Hello this is the main page"

if __name__ == "__main__":
	app.run()
```

### tutorial 1: intro
```python
from flask import Flask, redirect, url_for

app = Flask(__name__)
admin = True

@app.route("/")

def home():
    return "Hello this is the main page"

#variable
@app.route("/<name>")
def user(name):

    return f'hello {name}'

@app.route("/admin")
def admin():
    if admin == False:
	    #redirecring user with these 2 Flask methods
        return redirect(url_for("home"))
    else:
        return "hello admin man"
        
if __name__ == "__main__":
    app.run()
```

### tutorial 2: html templates
HTML template
```django
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Home page</title>
        <link rel="stylesheet" href="">
    </head>
    <body>
        <h1>hello !!</h1>
        <p>{{content}}</p>
        {% for i in names %}
            <p>{{i}}</p>
            {% if i == 'wahab' %}<p>hello {{i}}</p>{% endif %}
        {% endfor %}

    </body>
</html>
```

Flask code
```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/<name>')
def home(name):
    #render_template method to render html files
    return render_template('index.html',
                           content=f'your name: {name}',
                           names=['aziz','wahab','zyzz'])

if __name__ == "__main__":
    app.run(debug=True)
```
### tutorial 3: Bootstrap and Temple inheritance
Base template with [Bootstrap](https://getbootstrap.com/docs/4.3/getting-started/introduction/)
```django
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>{% block title %}{% endblock %}</title>
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    </head>
    <body>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <a class="navbar-brand" href="{{ url_for('home') }}">Virtual Plaza</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav mr-auto">
                <li class="nav-item">
                  <a class="nav-link" href="{{ url_for('server') }}">Server</a>
                </li>
              </ul>
            </div>
          </nav>
        {% block content %}{% endblock %}
        <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/popper.js@1.14.7/dist/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
    </body>
</html>
```
template inheritance with index
```django
{% extends 'base.html' %}

{% block title %}Home page{% endblock %}

{% block content %}
<h1>Welcome to home {{user}}</h1>
{% endblock %}
```
template inheritance with other page
```django
{% extends 'base.html' %}

{% block title %}Server{% endblock title %}

{% block content %}
{% for i in range(10) %}
    <p> server {{i**2}} </p>
{% endfor %}
{% endblock content %}
```
Flask code
```python
from flask import Flask, render_template, url_for

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html',
                           user='wahab')

@app.route('/server')
def server():
    return render_template('page.html')

@app.route('/<name>')
def hello(name):
    return f'hello ! "{name}" is an invalid link maybe ?'

if __name__ == "__main__":
    app.run(debug=True)
```
***
### tutorial 4: HTTP Methods (GET/POST) & Retrieving Form Data
login form page (extended from a base.html template)
```haml
{% extends 'base.html' %}

{% block title %}Login Page{% endblock title %}

{% block content %}
<form method="POST">
    <p>Username: </p>
    <p><input type='text' name='nm'></p>
    <p><input type='submit' value='submit'></p>
</form>
{% endblock content %}
```
Flask request code
```python
from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html",
                           name='Wahab')

@app.route("/login", methods=["POST", "GET"])
def login():
    if request.method == "POST":
        user = request.form["nm"]
        return redirect(url_for("user", usr=user))
    else:
        return render_template("login.html")

@app.route("/<usr>")
def user(usr):
    return f"<h1>{usr}</h1>"

if __name__ == "__main__":
    app.run(debug=True)
```

### tutorial 5: Sessions
Flask Session
```python
from flask import Flask, render_template, request, redirect, url_for, session
from datetime import timedelta

app = Flask(__name__)
app.secret_key = '123'
app.permanent_session_lifetime = timedelta(days=1)

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/login", methods=["POST", "GET"])
def login():
    if request.method == "POST":
        session.permanent = True
        user = request.form["nm"]
        session['user'] = user
        return redirect(url_for("user"))
    else:
        if 'user' in session:
            return redirect(url_for('user'))
        return render_template("login.html")

@app.route("/user")
def user():
    if 'user' in session:
        user = session['user']
        return f'<h1>{user}</h1>'
    else:
        return redirect(url_for('login'))

@app.route('/logout')
def logout():
    session.pop('user', None)
    return redirect(url_for('login'))

if __name__ == "__main__":
    app.run(debug=True)
```