# Ex.07 Restaurant Website
# Date:05-10-2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
```
index.html

{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Salamath Hotel</title>
  <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>
    <center>
    <div class="logo">
    <img src={% static "salamath.jpeg" %} alt="logo">
    </center>
  </div>

  <nav class="navbar">
    <a href="{% url 'index' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'admin' %}">Administration</a>
      <a href="{% url 'about' %}">About</a>

  </nav>

  <div class="banner">
    <img src={% static "30.png" %} alt="30% Off This Weekend">
  </div>

  <section class="cards">
    <div class="card">
      <img src={% static "mandhi.jpg" %} alt="Our New Menu">
      <h3>Our Signature Dish</h3>
      <p>Yemeni Mandhi is the signature dish of Salamath Hotel, renowned for its fragrant basmati rice, tender slow-cooked meat, and aromatic blend of spices. Every bite delivers an authentic taste of traditional Yemeni cuisine, making it a favorite among our guests</p>
    </div>

    <div class="card">
      <img src={% static "2.png" %} alt="Book a Table">
      <h3>Book a Table</h3>
      <p>Reserve your table at Salamath Hotel and enjoy an unforgettable dining experience. Whether it’s a family gathering or a special celebration, we ensure comfort, great service, and delicious meals every time</p>
      
    </div>

    <div class="card">
      <img src={% static "3.png" %} alt="Opening Hours">
      <h3>Opening Hours</h3>
      <p>Mon - Fri: 2pm - 10pm<br>Sat: 2pm - 11pm<br>Sun: 2pm - 9pm</p>
    </div>
  </section>

</body>
</html>

menu.html

{% load static %}

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu - Salamath Hotel</title>
  <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>
   
    <nav class="navbar">
      <a href="{% url 'index' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'admin' %}">Administration</a>
      <a href="{% url 'about' %}">About</a>
    </nav>
    <center>
          <h1>Our Dishes</h1>
    </center>

    <section class="cards">
      <div class="card">
        <img src={% static "mandhi.jpg" %} alt="Dish 1" width="50px" height="200px">
        <h3>Yemeni Mandhi</h3>
        <p>Fragrant basmati rice with tender meat and aromatic spices, our signature dish.</p>
      </div>
      <div class="card">
        <img src={% static "biriyani.jpg" %} alt="Dish 2" width="50px" height="200px">
        <h3>Chicken Biriyani</h3>
        <p>Spiced chicken cooked with fragrant basmati rice.</p>
      </div>
      <div class="card">
        <img src={%static "dosa.jpg" %} alt="Dish 3" width="50px" height="200px">
        <h3>Dosa</h3>
        <p>Crispy South Indian crepe made from fermented rice and lentil batter, served with chutney and sambar.</p>
      </div>
      <div class="card">
        <img src={%static "fish.jpg" %} alt="Dish 4" width="50px" height="200px">
        <h3>Fish curry</h3>
        <p>Fresh fish simmered in a tangy and spicy coconut-based curry, bursting with flavor.</p>
      </div>
      <div class="card">
        <img src={%static "friedrice.jpg" %} alt="Dish 5" width="50px" height="200px">
        <h3>Fried Rice</h3>
        <p>Stir-fried rice with vegetables, eggs, and your choice of meat, seasoned with aromatic sauces.</p>
      </div>
      <div class="card">
        <img src={%static "meals.jpg" %} alt="Dish 6" width="50px" height="200px">
        <h3>Meals</h3>
        <p>Traditional South Indian meals served on a banana leaf, featuring rice, curries, sambar, and pickles.</p>
      </div>
      <div class="card">
        <img src={%static "mutton biriyani.jpg" %} alt="Dish 7" width="50px" height="200px">
        <h3>Mutton Biriyani</h3>
        <p>Slow-cooked mutton blended with aromatic rice and traditional spices for a rich, flavorful taste.</p>
      </div>
      <div class="card">
        <img src={%static "noodles.jpg" %} alt="Dish 8" width="50px" height="200px">
        <h3>Noodles</h3>
        <p>Soft, stir-fried noodles tossed with vegetables and sauces, customizable with chicken, shrimp, or veg.</p>
      </div>
      <div class="card">
        <img src={%static "porotta.jpg" %} alt="Dish 9" width="50px" height="200px">
        <h3>Porotta</h3>
        <p>Flaky, layered flatbread, soft on the inside and slightly crispy outside, perfect with curries.</p>
      </div>
      <div class="card">
        <img src={%static "prawn.jpg" %} alt="Dish 10" width="50px" height="200px">
        <h3>Prawn fry</h3>
        <p>Succulent prawns marinated with spices and fried to golden perfection, a seafood delight.</p>
      </div>
      <div class="card">
        <img src={%static "shawarma.jpg" %} alt="Dish 11" width="50px" height="200px">
        <h3>Shawarma</h3>
        <p>Thinly sliced spiced meat wrapped in soft flatbread, served with fresh veggies and sauce.</p>
      </div>
      <div class="card">
        <img src={%static "thandoori.jpg" %} alt="Dish 12" width="50px" height="200px">
        <h3>Chicken Thandoori</h3>
        <p>Juicy chicken marinated in yogurt and spices, roasted in a traditional tandoor for smoky flavor.</p>
      </div>
    </section>
</body>
</html>

admin.html

{% load static %}

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Administration - Salamath Hotel</title>
  <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>
   

    <nav class="navbar">
      <a href="{% url 'index' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'admin' %}">Administration</a>
      <a href="{% url 'about' %}">About</a>
    </nav>
    <center>
          <h1>Administration</h1>
    </center>
    <center>
    <section class="cards">
      <div class="card">
        <img src={% static "azar2.jpeg" %} alt="Staff 1 " width="50px" height="300px" >
        <h3>Azar - CEO</h3>
      </div>
      <div class="card">
        <img src={% static "abdul.jpeg" %} alt="Staff 2" width="50px" height="300px" >
        <h3>Razik - Manager</h3>
      </div>
      <div class="card">
        <img src={% static "johmson.jpeg" %} alt="Staff 3" width="50px" height="300px">
        <h3>Johmson - Chef</h3>
      </div>
      <div class="card">
        <img src={% static "deva.jpeg" %} alt="Staff 7" width="50px" height="300px">
        <h3>Deva - Chef </h3>
      </div>
      <div class="card">
        <img src={% static "salman.jpeg" %} alt="Staff 4" width="50px" height="300px">
        <h3>Salman - Waiter</h3>
      </div>
      <div class="card">
        <img src={% static "vgp.jpeg" %} alt="Staff 5" width="50px" height="300px">
        <h3>Vishnu - Waiter</h3>
      </div>
      <div class="card">
        <img src={% static "kumara.jpeg" %} alt="Staff 6" width="50px" height="300px">
        <h3>Kumara - Reception</h3>
      </div>
    </section>
    
   
    </center>
</body>
</html>


about.html

{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About - Salamath Hotel</title>
  <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>
   

    <nav class="navbar">
      <a href="{% url 'index' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'admin' %}">Administration</a>
      <a href="{% url 'about' %}">About</a>
    </nav>
        <center>
        <h1>About Salamath Hotel</h1>
        <h4>Salamath Hotel is famous for its authentic Yemeni Mandhi, our signature dish, and other delicious meals.</h4>
        <h4>We aim to provide a warm and memorable dining experience for all our guests.</h4>
        <h4>Our team is dedicated to using fresh ingredients and delivering excellent service every time.</h4>
        </center>
        <h3>Contact Us</h3>
        <p><strong>Address:</strong> 123 Main Road,SP Pattinam, Ramanathapuram dist 623406</p> 
        <p><strong>Phone:</strong> +91 8015137032</p>
        <p><strong>Email:</strong> info@salamathhotel.com</p>
        <p><strong>Website:</strong> www.salamathhotel.com</p>
     
</body>
</html>

style.css

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: aqua;
}

.navbar {
  background-color: #333;
  display: flex;
  justify-content: center;
}
.navbar a {
  color: red;
  text-decoration: none;
  padding: 15px 25px;
  display: inline-block;
}
.navbar a:hover {
  background-color: #555;
}

.banner img {
  width: 100%;
  height: auto;
  display: block;
}

.logo img {
  height: 20%;
  width: 100%;
  height: auto;
  display: block;
}
.cards {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 20px;
  background: aqua;
}
.card {
  width: 300px;
  background: #ffeedd;
  border-radius: 8px;
  padding: 15px;
  margin: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;

}
.card:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 15px rgba(0,0,0,0.2);
  cursor: pointer;
}

.card img {
  width: 100%;
  border-radius: 6px;
  margin-bottom: 10px;
}
.card h3 {
  margin-bottom: 10px;
}
.card p {
  font-size: 14px;
  margin-bottom: 10px;

}
.card a {
  color: blue;
  text-decoration: none;
}
.card a:hover {
  text-decoration: underline;
}

@media (max-width: 768px) {
  .cards {
    flex-direction: column;
    align-items: center;
  }
}

views.py

from django.shortcuts import render

def index(request):
    return render(request,'index.html')
def menu(request):
    return render(request,'menu.html')
def admin(request):
    return render(request,'admin.html')
def about(request):
    return render(request,'about.html')


urls.py

from django.urls import path
from myapp import views
urlpatterns = [
    path('',views.index,name='index'),
    path('menu/',views.menu ,name='menu'),
    path('admin/',views.admin ,name='admin'),
    path('about/',views.about ,name='about'),
]
```
# OUTPUT:
azar/website/1.png
![alt text](2.1.png)
azar/website/3.png
azar/website/4.png
azar/website/5.png
# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
