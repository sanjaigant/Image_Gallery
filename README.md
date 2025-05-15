# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM

~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>my favourites</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>my favourites ❤️</h1>
  <div class="gallery">
    <div class="card">
      <img src="Screenshot 2025-05-15 082642.png" alt="Superstar">
      <p>Superstar</p>
    </div>
    <div class="card">
      <img src="Screenshot 2025-05-15 083114.png" alt="thala">
      <p>thala</p>
    </div>
    <div class="card">
      <img src="Screenshot 2025-05-15 083259.png" alt="ceo of google">
      <p>ceo of google</p>
    </div>
    <div class="card">
      <img src="Screenshot 2025-05-15 083431.png" alt="Arnold">
      <p>Arnold</p>
    </div>
    <div class="card">
      <img src="Screenshot 2025-05-15 083553.png" alt="spb">
      <p>spb</p>
    </div>
  </div>

  <div id="lightbox" class="lightbox">
    <span class="close">&times;</span>
    <img id="lightbox-img" src="">
    <div id="lightbox-caption"></div>
  </div>

  <script src="script.js"></script>
</body>
</html>
const cards = document.querySelectorAll('.card img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const lightboxCaption = document.getElementById('lightbox-caption');
const closeBtn = document.querySelector('.close');

cards.forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'flex';
    lightboxImg.src = img.src;
    lightboxCaption.textContent = img.alt;
  });
});

closeBtn.addEventListener('click', () => {
  lightbox.style.display = 'none';
});

window.addEventListener('click', (e) => {
  if (e.target === lightbox) {
    lightbox.style.display = 'none';
  }
});
body {
    background: black;
    overflow: hidden;
  }
  
  body::before {
    content: "";
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: url("https://www.transparenttextures.com/patterns/stardust.png");
    opacity: 0.2;
    z-index: -1;
  }
  
  
  h1 {
    font-size: 2.5em;
    color:seashell;
    margin-bottom: 40px;
  }
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
    padding: 20px;
  }
  
  
  .card {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    border: 1px solid rgba(255, 255, 255, 0.2);
    transition: transform 0.3s ease;
  }
  
  
  
  .card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: transform 0.3s ease;
  }
  
  .card img:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  
  .card p {
    margin: 0;
    padding: 10px;
    font-weight: bold;
    color: #444;
    background-color: rgba(255,255,255,0.6);
  }
  
  /* Lightbox styles */
  .lightbox {
    display: none;
    position: fixed;
    top: 0; left: 0;
    width: 100vw;
    height: 100vh;
    backdrop-filter: blur(15px);
    background: rgba(0, 0, 0, 0.7);
    justify-content: center;
    align-items: center;
    flex-direction: column;
    z-index: 1000;
  }
  
  .lightbox img {
    max-width: 90%;
    max-height: 80vh;
    border-radius: 10px;
  }
  
  .lightbox .close {
    position: absolute;
    top: 30px;
    right: 40px;
    font-size: 40px;
    color: white;
    cursor: pointer;
  }
  
  #lightbox-caption {
    margin-top: 20px;
    color: #fff;
    font-size: 1.2em;
  }
  
  .gallery {
    animation: fadeIn 0.8s ease-in-out;
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
~~~

## OUTPUT
![alt text](image.png)
![alt text](<Screenshot 2025-05-15 084820.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
