---
layout: post
title: Routing in Flask Application
date: 2021-08-27
categories: flask python
---

# Routes in Flask

> This is post is continuation of [this post]()

A fully functional website has multiple routes like `/about` for About page or `/contact` for contact Page.

We can create routes in Flask by calling `route` function on our `app` function. First argument of this function is the endpoint. It always start with a forward slash &mdash; `/<route>`

Let's see this in action by creating a `/about` route to our hello world application. Right now your `app.py` file should look like this.

```py
from  flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "Hello World"

if __name__ = "__main__":
    app.run(debug=True)
```

We pass `debug=True` in `app.run()` so that it automatically detect the changes and restart the app.

Now add the code for `/about` route down below `/` route and above `if` statement.

```py
@app.route('/about')
def about():
    return "This is About page"
```

Open your browser and go the following link &mdash; `localhost:5000/about`. You should see the following output.

<!-- image for about route -->

<br>

## Todo for you

Add a route for contact page and display "You are on contact page".

Once you are done check your answer down below.

Code for `/contact` route

```python
@app.route("/contact")
def contact():
    return "You are on contact page"
```

<br>

We can also create nested routes like `/auth/login` or `/users/pysimplify`. Let's see this in action.

```python
@app.route('/auth/login')
def login():
    return "You are on login Page"
```

Navigate to `localhost:5000/auth/login` to view this page in your browser. You should see something like this .

<!-- image for /auth/login -->

So far we have covered how to create simple routes and nested routes. Now we will see how to use variable routes i.e. using varaible in routess.

For example: `/user/<user-num>`
