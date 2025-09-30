# Build-a-Portfolio-Website-with-Flask
Create a personal portfolio site
Project Structure
portfolio/
│── app.py
│── templates/
│    ├── index.html
│    ├── about.html
│    ├── projects.html
│    └── contact.html
│── static/
│    ├── css/
│    │    └── style.css
│    └── images/
│         └── profile.jpg
Step 1: Install Flask
pip install flask
Step 2: Create app.py
from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/about")
def about():
    return render_template("about.html")

@app.route("/projects")
def projects():
    return render_template("projects.html")

@app.route("/contact")
def contact():
    return render_template("contact.html")

if __name__ == "__main__":
    app.run(debug=True)
Step 3: Create Templates (templates/)
index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Portfolio</title>
  <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
  <header>
    <h1>Hi, I'm Siddartha 👋</h1>
    <nav>
      <a href="/">Home</a>
      <a href="/about">About</a>
      <a href="/projects">Projects</a>
      <a href="/contact">Contact</a>
    </nav>
  </header>
  <section>
    <h2>Welcome to My Portfolio</h2>
    <p>This is where I showcase my work and skills.</p>
  </section>
</body>
</html>
about.html
{% extends "index.html" %}
{% block content %}
<h2>About Me</h2>
<p>I am a passionate developer learning Flask and building web apps.</p>
{% endblock %}
Step 4: Add CSS (static/css/style.css)
body {
  font-family: Arial, sans-serif;
  margin: 0; padding: 0;
  background: #f4f4f9;
}

header {
  background: #333;
  color: white;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

section {
  padding: 20px;
}
body {
  font-family: Arial, sans-serif;
  margin: 0; padding: 0;
  background: #f4f4f9;
}

header {
  background: #333;
  color: white;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

section {
  padding: 20px;
}
body {
  font-family: Arial, sans-serif;
  margin: 0; padding: 0;
  background: #f4f4f9;
}

header {
  background: #333;
  color: white;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

section {
  padding: 20px;
}
body {
  font-family: Arial, sans-serif;
  margin: 0; padding: 0;
  background: #f4f4f9;
}

header {
  background: #333;
  color: white;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

section {
  padding: 20px;
}
Step 5: Run the App
python app.py
