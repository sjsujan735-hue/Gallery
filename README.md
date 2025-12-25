# Ex.08 Design of Interactive Image Gallery
# Date:13/12/25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<html>
    <head>
    <title>Image Gallery</title>
    <style>
        body {
           
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #add8e6; /* Light blue */
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
}

        

        .header {
            text-align: center;
            padding: 10px;
            background-color: #1ba1e4a4;
            width: 100%;
            height:100px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            font-family:monospace;
        
        }

        .header h1 {
            font-size: 2.5rem;
            color: #9c28a9;
        }

        .header p {
            font-size: 1.2rem;
            color:#000000;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
            margin: 20px 0 10px 0;
            width: 90%;
            max-width: 1200px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            border: 10px solid #2897d6;
            margin-right: 40px;
        }

        .gallery-item img {
            width: 100%;
            height:100%;
            object-fit: cover;
            display: block;
        }

        .gallery-item:nth-child(1) {
            grid-column: span 2;
            grid-row: span 2;
        }

        .gallery-item:nth-child(3) {
            grid-column: span 2;
        }

        .gallery-item:nth-child(6) {
            grid-column: span 2;
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom right, rgba(255, 255, 255, 0.2), rgba(0, 0, 0, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            width: 100%;
            height:40px;
            background-color: #1d9ae8;
        }

        .footer p{
            font-size: 1.2rem;
            color: #000000;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox:target {
            display: flex;
        }

        #lightbox .close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #1aade8;
            border: none;
            font-size: 2rem;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Image Gallery</h1>
   
</div>

<div class="gallery">
    <div class="gallery-item" onclick="showAlert('Image 1 clicked!')">
        <img src="c:\Users\admin\Downloads\shih-tzu-temperament.jpeg-900x510.jpg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 2 clicked!')">
        <img src="c:\Users\admin\Downloads\KOA_Nassau_2697x1517.jpg" alt="Image 2" >
    </div>
    <div class="gallery-item" onclick="showAlert('Image 3 clicked!')">
        <img src="c:\Users\admin\Downloads\hq720.jpg"alt="Image 3">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 4 clicked!')">
        <img src="c:\Users\admin\Downloads\images.jpeg" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 5 clicked!')">
        <img src="c:\Users\admin\Downloads\images (1).jpeg" alt="Image 5">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 6 clicked!')">
        <img src="c:\Users\admin\Downloads\Shih-Tzu.jpg" alt="Image 6">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 7 clicked!')">
        <img src="c:\Users\admin\Downloads\istockphoto-1250262738-2048x2048.jpg"  alt="Image 7">
    </div>
    
    <div class="gallery-item" onclick="showAlert('Image 8 clicked!')">
        <img src="c:\Users\admin\Downloads\istockphoto-476533275-612x612.jpg" alt="Image 8">
    </div>
</div>

<div id="lightbox">
    <button class="close" onclick="closeLightbox()">&#215;</button>

    <img src="" id="lightbox-img" alt="Full Image">
</div>

<div class="footer">
    <p><b>Designed by Safira Barveen</b></p>
</div>

<script>
    function showAlert(message) {
        alert(message);
    }

    function openLightbox(imageSrc) {
        document.getElementById('lightbox-img').src = imageSrc;
        document.getElementById('lightbox').style.display = 'flex';
    }

    function closeLightbox() {
        document.getElementById('lightbox').style.display = 'none';
    }

    const galleryItems = document.querySelectorAll('.gallery-item');
    galleryItems.forEach(item => {
        item.addEventListener('click', () => {
            const imgSrc = item.querySelector('img').src;
            openLightbox(imgSrc);
        });
    });
</script>

</body>
</html>


```
# OUTPUT:
<img width="1823" height="1083" alt="397365338-d56a07f7-e1b9-44ae-817e-3f656aa89c6b -2" src="https://github.com/user-attachments/assets/b9a80bef-a2da-49af-a4cc-337cdf2753ca" />
<img width="1815" height="1069" alt="397365585-f3b03571-d53e-47ad-a8a8-be06ca825d8c" src="https://github.com/user-attachments/assets/8555aa4e-a944-4580-a843-270b9bd00acc" />
<img width="1824" height="1022" alt="397365810-64ef6446-595b-4605-be53-3341abd0c16c" src="https://github.com/user-attachments/assets/4a4e85a2-dac8-43fb-9622-9afb457524d8" />
<img width="1758" height="970" alt="397365964-73955860-1c4c-465c-8e3e-ca36eddcf740" src="https://github.com/user-attachments/assets/5fbbd43d-83fb-4b03-aa60-b89fda565cdf" />
<img width="1825" height="994" alt="397366478-c14a99f5-f6a0-4411-a768-dcd0e311de74" src="https://github.com/user-attachments/assets/45708aae-c016-453f-8c12-a4efc5fbd874" />
<img width="1839" height="1062" alt="397366642-cc21dc74-bc86-4ee7-87a0-27f822908c8d" src="https://github.com/user-attachments/assets/00372b35-d747-414d-ba31-d6d8c0c1de56" />
<img width="1842" height="681" alt="397366874-16280f95-797b-4457-9ce8-7e296c7f774b" src="https://github.com/user-attachments/assets/ff90c199-5061-4be8-8f85-594f5c96a791" />



# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
