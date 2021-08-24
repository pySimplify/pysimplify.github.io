---
layout: post
title: Hello World Flask Application
date: 2021-08-25
categories: flask python
---

# What is a Flask

Flask is a microframework for Python. It is a thin layer on top of the standard Python Web Server, WSGI, and the web application itself. Flask is designed to make it easy to create small web applications. Check out the [Flask Documentation](https://flask.palletsprojects.com/en/1.1.x/).

<br />

# Flask Installation using pip

> python3 is required.

```bash
pip install flask
```

If you already have flask installed, make sure you have the latest version.

```bash
pip install --upgrade flask
```

<br />
# Create you flask app

Open a new terminal window and navigate to the directory where you want to create your flask app. You can create a new directory with the following command:

```bash
mkdir flask_app
cd flask_app
```

Now create a new file called `app.py` and paste the following code into it:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "Hello World!"


if __name__ == "__main__":
    app.run()
```

In the terminal, run the following command to run the app:

```bash
python app.py
```

You should see the following output:

```bash
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

Copy the url(`http://127.0.0.1:5000/`) from the output and paste it into your browser. You should see the following output:

![flask browser image](/assets/hello-flask.png)

Voila! You have created a simple flask app.
