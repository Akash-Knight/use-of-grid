# My Gallery Website

## Description
This is a simple gallery website project that displays images in a stylish and responsive layout. It features hover effects on the images and image captions using HTML and CSS.

## Features
- Responsive design.
- Hover effects on images (scaling and color transition).
- Image captions appear on hover.
- Clean and minimalist layout.

## Project Structure
The project consists of two files:
1. `index.html` - The main HTML file that structures the gallery.
2. `project9.css` - The CSS file that styles the gallery and adds animations.

### HTML (`index.html`)
The HTML file contains:
- A header with the title "My Gallery".
- A gallery grid with images and their captions.
- The gallery is wrapped in a `<div>` with the class `wrapper`, which contains a `container` for better layout management.

### CSS (`project9.css`)
The CSS file includes:
- Basic resets for margins and padding.
- A responsive grid layout using flexbox for the gallery.
- Hover effects on each image:
  - Grayscale effect on images by default.
  - Zoom-in and grayscale removal on hover.
  - Captions appear with a fade-in effect.

## Usage
1. Clone the repository.
   ```bash
   git clone https://github.com/your-username/my-gallery.git
## File Structure

├── index.html
└── project9.css

## HTML FILE


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Gallery</title>
    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="project9.css">
</head>
<body>

    <div class="wrapper">

        <div class="container">
            <h1>My Gallery</h1>

            <div class="gallery">
                <figure class="card">
                    <img src="image1.jpg" alt="image1">
                    <figcaption>image 1</figcaption>
                </figure>
                <figure class="card">
                    <img src="image2.jpeg" alt="image2">
                    <figcaption>image 2</figcaption>
                </figure> 
                <figure class="card">
                    <img src="image4.jpeg" alt="image3">
                    <figcaption>image 3</figcaption>
                </figure> 
                <figure class="card">
                    <img src="image5.jpeg" alt="image4">
                    <figcaption>image 4</figcaption>
                </figure>
                <figure class="card">
                    <img src="image6.jpeg" alt="image5">
                    <figcaption>image 5</figcaption>
                </figure> 
                <figure class="card">
                    <img src="image7.jpeg" alt="image6">
                    <figcaption>image 6</figcaption>
                </figure> 
                <figure class="card">
                    <img src="image8.jpeg" alt="image7">
                    <figcaption>image 7</figcaption>
                </figure> 
                <figure class="card">
                    <img src="image9.jpeg" alt="image8">
                    <figcaption>image 8</figcaption>
                </figure>
                <figure class="card">
                    <img src="image11.jpg" alt="image9">
                    <figcaption>image 9</figcaption>
                </figure>
            </div>

        </div>
    </div>
    
</body>
</html>

## CSS FILE


        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
    
          }

      .wrapper{
              height: 100vh;
              overflow-x: hidden;
              overflow-y: auto;
             }

      .container{
               height: 100%;
               max-width:1200px;
               margin:0 auto;
               padding: 20px;
             }

       .container h1{
    margin:15px;
    text-align: center;
    font-size:3rem;
    }

    .gallery{
    margin: auto 0;
    display: flex;
    flex-wrap:wrap;
    justify-content:space-evenly;
    }

    .card{
    width: 30%;
    position: relative;
    margin-bottom: 20px;
    border-radius: 10px;
    overflow: hidden;
    }

    .card img{
    height: 100%;
    width: 100%;
    filter: grayscale(75%);
    box-shadow: 0 0 20px #333;
    object-fit: cover;
    }

    .card:hover{
    transform: scale(1.09);
    transition: 0.9s;
    filter: drop-shadow(0 0 10px #333);
    }

    .card:hover img{
    filter: grayscale(0%);
    }

    .card figcaption{
    position: absolute;
    bottom: 0;
    left: 0;
    padding:25px;
    width: 100%;
    height:20%;
    color:rgb(250, 250, 250);
    font-weight: 500px;
    font-size: 15px;
    opacity: 0;
    border-radius: 0 0 10px;
    background: linear-gradient(rgb(72, 68,2), rgb(56, 56, 10));
    transition:0.9s;
    letter-spacing:2px;
    text-transform: uppercase;
    }

    .card:hover figcaption{
    opacity: 1;
    transform: scale(1.09);
    }


