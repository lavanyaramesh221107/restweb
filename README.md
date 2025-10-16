# Ex.07 Restaurant Website
## Date:11.10.2025
## lavanya R
## 25017651

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
# Ex.07 Restaurant Website

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
'''
base.html

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>{% block title %}Spice Delight{% endblock %}</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  margin: 0; padding: 0;
}

header {
  background-color: #c0392b;
  padding: 10px;
  color: white;
}

nav ul {
  list-style: none;
  text-align: center;
  padding: 0;
}

nav ul li {
  display: inline-block;
  margin: 0 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

.banner {
  width: 100%;
  height: 300px;
  object-fit: cover;
}

.intro {
  padding: 40px;
  text-align: center;
}

.menu-grid, .team-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  padding: 20px;
}

.menu-grid .item img, .team-grid .member img {
  width: 100%;
  border-radius: 10px;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
}

</style>

</head>
<body>
  <header>
    <img src="banner.jpg" alt="Banner" class="banner">
    <nav>
      <ul>
        <li><a href="home.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="administration.html">Administration</a></li>
        <li><a href="contact.html">Contact Us</a></li>
      </ul>
    </nav>
  </header>

  <main>
    {% block content %}{% endblock %}
  </main>

  <footer>
    <p>Designed by Your Name © 2025</p>
  </footer>
</body>
</html>
home.html
{% extends 'base.html' %}
{% block title %}Home — Spice Delight{% endblock %}
{% block content %}
<section class="intro">
  <h1>Welcome to Spice Delight</h1>
  <p>Serving traditional flavors with a modern twist. Join us for an unforgettable experience.</p>
</section>
{% endblock %}
menu.html
{% extends 'base.html' %}
{% block title %}Menu — Spice Delight{% endblock %}
{% block content %}
<section class="menu">
  <h2>Our Menu</h2>
  <div class="menu-grid">
    {% for food in foods %}
      <div class="item">
        <img src="food.jpg" alt="{{ food.name }}">
        <p>{{ food.name }}</p>
      </div>
    {% endfor %}
  </div>
</section>
{% endblock %}
administration.html
{% extends 'base.html' %}
{% block title %}Administration — Spice Delight{% endblock %}
{% block content %}
<section class="team">
  <h2>Our Team</h2>
  <div class="team-grid">
    {% for member in team %}
      <div class="member">
        <img src="crew.jpg" alt="{{ member.name }}">
        <p>{{ member.name }} – {{ member.role }}</p>
      </div>
    {% endfor %}
  </div>
</section>
{% endblock %}
contact.html
{% extends 'base.html' %}
{% block title %}Contact Us — Spice Delight{% endblock %}
{% block content %}
<section class="contact">
  <h2>Contact Us</h2>
  <p>📍 Address: {{ contact.address }}</p>
  <p>📞 Phone: {{ contact.phone }}</p>
  <p>✉️ Email: {{ contact.email }}</p>
</section>
{% endblock %}

home.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #007BFF;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 36px;
        }
        nav {
            background-color: #0056b3;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            max-width: 900px;
            margin: 20px auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        p {
            text-align: justify;
            color: #555;
            font-size: 16px;
            line-height: 1.6;
        }
        footer {
            background-color: #007BFF;
            color: white;
            text-align: center;
            padding: 15px 0;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Institution</h1>
    </header>

    <nav>
        <a href="home.html">Home</a>
        <a href="administration.html">Administration</a>
        <a href="contact.html">Contact</a>
    </nav>

    <div class="container">
        <p>
            Welcome to our institution! We are dedicated to providing high-quality education
            and fostering an environment where students can grow academically, socially, and
            personally. Our faculty and staff are committed to guiding students to achieve
            their full potential through a variety of programs, activities, and support services.
        </p>
        <p>
            Explore our website to learn more about our administration, courses, and ways
            to get in touch with us. We strive to make your experience informative, engaging,
            and inspiring.
        </p>
    </div>

    <footer>
        &copy; 2025 Our Institution. All rights reserved.
    </footer>
</body>
</html>

menu.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #28a745;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        header h1 {
            margin: 0;
        }
        .menu-container {
            max-width: 600px;
            margin: 40px auto;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            padding: 20px;
            text-align: center;
        }
        .menu-container a {
            display: block;
            background-color: #28a745;
            color: white;
            padding: 12px;
            margin: 10px 0;
            text-decoration: none;
            border-radius: 5px;
            font-size: 18px;
            transition: 0.3s;
        }
        .menu-container a:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <header>
        <h1>Main Menu</h1>
    </header>

    <div class="menu-container">
        <a href="home.html">Home</a>
        <a href="administration.html">Administration</a>
        <a href="contact.html">Contact</a>
        <a href="about.html">About Us</a>
        <a href="gallery.html">Gallery</a>
    </div>
</body>
</html>

contact.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            background: #fff;
            padding: 30px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            border-radius: 8px;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        label {
            margin-top: 10px;
            font-weight: bold;
            color: #555;
        }
        input, textarea {
            margin-top: 5px;
            padding: 10px;
            font-size: 16px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        textarea {
            resize: vertical;
            min-height: 100px;
        }
        button {
            margin-top: 20px;
            padding: 12px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .info {
            margin-top: 20px;
            text-align: center;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Contact Us</h1>
        <form action="#" method="post">
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" placeholder="Your Name" required>

            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" placeholder="Your Email" required>

            <label for="message">Message:</label>
            <textarea id="message" name="message" placeholder="Write your message here..." required></textarea>

            <button type="submit">Send Message</button>
        </form>
        <div class="info">
            <p>Email: info@example.com | Phone: +91 12345 67890</p>
            <p>Address: 123, Example Street, City, Country</p>
        </div>
    </div>
</body>
</html>

administration.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Administration</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 900px;
            margin: 40px auto;
            background-color: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        p {
            text-align: justify;
            font-size: 16px;
            color: #555;
            line-height: 1.6;
        }
        ul {
            margin: 20px 0;
            padding-left: 20px;
        }
        li {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Administration</h1>
        <p>
            The administration department is responsible for the smooth operation and management
            of the institution. It oversees academic and non-academic activities, manages
            resources, and ensures compliance with policies and regulations. The administrative
            team is committed to providing support to both students and faculty.
        </p>
        <h2>Key Offices:</h2>
        <ul>
            <li>Principal's Office</li>
            <li>Finance and Accounts</li>
            <li>Admissions Office</li>
            <li>Student Services</li>
            <li>Human Resources</li>
        </ul>
        <p>
            Our goal is to maintain an organized, transparent, and efficient administration
            that supports the educational mission and overall growth of the institution.
        </p>
    </div>
</body>
</html>

'''

## OUTPUT:
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/570d073e-75d5-421c-9b00-fd871427048e" />) 
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9d79d40c-b0ad-4a0a-9158-06fd872aeba4" />) 
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0cb4c8cc-c695-4251-bdf6-7dc501e43346" />) 
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e73bbd7c-1cc9-4909-a2f3-00956012f4ae" />) 
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fc001961-d2d0-4603-b4bf-846cdc851390" />) 
![alt text](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9277b5a2-0875-4909-aa81-476c24373362" />)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.

