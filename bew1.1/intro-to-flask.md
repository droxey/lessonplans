# 📜 Day 7: Introduction to Web Servers in Flask

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Flask_logo.svg" height="150">
</p>

<!--
What students know so far...

Week 1
    1. [BEW] Static website (static HTML/basic CSS, chrome inspector)
    2. [BEW] Git & GitHub
    3. [CS] Variables, Functions, and Program Design
    4. [CS] Control Flow and Lists
Week 2
    1. [CS] Pseudocode and Flowchart Diagrams
    2. [BEW] Request-Response Cycle and MVC Architecture


TODO: Flask Starter Pack with pre-built static front end

TODO: Questions for Alan:
  - Will they know how to import Python packages by Day 7?
  - Will they know virtual environments? Should they yet?
  -
-->

### ⏱ Agenda

1. [🏆 Learning Objectives](#%f0%9f%8f%86-learning-objectives)
2. [📖 Overview](#%f0%9f%93%96-overview)
3. [Sample](#sample)
4. [🌴 [10m] Break -->](#%f0%9f%8c%b4-10m-break)
5. [🌃 After Class](#%f0%9f%8c%83-after-class)
6. [📚 Resources & Credits](#%f0%9f%93%9a-resources--credits)

## 🏆 Learning Objectives

1. Define what a web server is and what role it plays on the internet
1. Describe what the Flask framework is and how to use it
1. Differentiate between frontend and backend stacks
1. Understand how Python works into HTML/CSS

## 📖 Overview

<!--
- TT: overview of how we learned basic frontend, but how do we drive it forward? What about data?
- TT: Overview of Flask: what it is, why we use it
-->

### Making A Static Site Dynamic

#### Step by Step

1. Use `flask-starterpack` to demonstrate how to make a static site dynamic
2. Explain why static HTML and CSS  goes in the `static` folder
3. Serve the static HTML page via `http://localhost:8000/index.html` first
4. Ask "How many URLs have `.html` at the end of them these days?"
   1. Clean URLs / Semantic URLs definition and why we use them
5. Show how to serve the template in the `templates` directory with Flask

### Adding a Python Function to the Project

<!-- TT: Review of Python, you all were introduced to this via prework -->
<!-- Activity: some easy interview problem to solve in Python to get them warmed up again -->

#### Step by Step

1. Start in the directory that contains a pre-made static site
2. Demo the static site in the browser and explain that we'll be making this static site dynamic today using Python and Flask
3. TODO: Define the problem we'll solve
4. Create a file named `app.py` and explain that this is where the code will live

    ```bash
    touch app.py
    ```

5. Define a problem then think / pair / share the function to solve it. Solution below:

    ```python
    ```

### Endpoints: How to Call a Function on the Web

<!-- TT: Python is our backend (what’s a backend?) HTML/CSS is our frontend (what’s a frontend?) -->

#### Step by Step

1. Add `@app.route` to the top of the function definition and explain that this **decorator** on top of the function makes it an **endpoint**:

    ```python
    ```

2. Add flask imports:

    ```python
    ```

3. Define `app` variable:

    ```python
    ```

4. Finally define `__main__`:

    ```python
    ```

5. Demo the function by running `flask run` on the terminal:

    ```bash
    ```

## Sample

```python
# 1. import Flask
from flask import Flask

# 2. Create an app, being sure to pass __name__
app = Flask(__name__)

# 3. Define what to do when a user hits the index route
@app.route("/")
def home():
    print("Server received request for 'Home' page...")
    return "Welcome to my 'Home' page!"

# 4. Define what to do when a user hits the /about route
@app.route("/about")
def about():
    print("Server received request for 'About' page...")
    return "Welcome to my 'About' page!"

if __name__ == "__main__":
  app.run(debug=True)
```

<!-- ## 💻 Activity


- Activity: first 2 chapters of this tutorial

## 🌴 [10m] Break -->

## 🌃 After Class


HW: create a design/outline for a simple Gif search site that returns a list of gifs from the Tenor API based off of a search query


## 📚 Resources & Credits

- https://blog.codeanalogies.com/2018/04/26/web-servers-explained-by-running-a-microbrewery/
- https://en.wikipedia.org/wiki/Flask_(web_framework)
- https://github.com/pallets/flask
- https://flask.palletsprojects.com/en/1.1.x/
