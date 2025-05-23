# Ex.08 Design of Interactive Image Gallery
## date:18-05-25

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
```
INDEX.HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Interactive Photo Gallery</title>
  <link rel="stylesheet" href="style.css" />
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .gallery-container {
      display: flex;
      overflow-x: auto;
      gap: 10px;
      padding: 20px;
      justify-content: center;
      align-items: center;
    }

    .gallery-item {
      flex: 0 0 auto;
      width: 200px;
      height: 150px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(51, 51, 51, 0.9);
      justify-content: center;
      align-items: center;
    }

    .modal.active {
      display: flex;
    }

    .modal img {
      max-width: 80%;
      max-height: 80%;
      border-radius: 10px;
    }

    .modal .close {
      position: absolute;
      top: 20px;
      right: 30px;
      color: white;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <div class="gallery-container" id="gallery">
    <div class="gallery-item"><img src="1.jpg" alt="Image 1" /></div>
    <div class="gallery-item"><img src="2.jpg" alt="Image 2" /></div>
    <div class="gallery-item"><img src="3.jpg" alt="Image 3" /></div>
    <div class="gallery-item"><img src="4.jpg" alt="Image 4" /></div>
    <div class="gallery-item"><img src="5.jpg" alt="Image 5" /></div>
  </div>

  <div class="modal" id="modal">
    <span class="close" id="closeBtn">&times;</span>
    <img id="modal-img" src="" alt="Enlarged Image" />
  </div>

  <script>
    const modal = document.getElementById("modal");
    const modalImg = document.getElementById("modal-img");
    const closeBtn = document.getElementById("closeBtn");
    const images = document.querySelectorAll(".gallery-item img");

    images.forEach((img) => {
      img.addEventListener("click", () => {
        modal.classList.add("active");
        modalImg.src = img.src;
      });
    });

    closeBtn.addEventListener("click", () => {
      modal.classList.remove("active");
    });

    modal.addEventListener("click", (e) => {
      if (e.target === modal) {
        modal.classList.remove("active");
      }
    });
  </script>
</body>
</html>


```

## OUTPUT
![alt text](<Screenshot 2025-05-18 221017.png>)

![alt text](<Screenshot 2025-05-18 221032.png>)

![alt text](<Screenshot 2025-05-18 221059.png>)

![alt text](<Screenshot 2025-05-18 221128.png>)

![alt text](<Screenshot 2025-05-18 221229.png>)

![alt text](<Screenshot 2025-05-18 221246.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
