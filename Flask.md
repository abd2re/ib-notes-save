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
---

### tutorial 2: html templates
HTML template
```html
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
        <p>{{r}}</p>

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
***
### tutorial 3: Bootstrap and Temple inheritance
HTML template

