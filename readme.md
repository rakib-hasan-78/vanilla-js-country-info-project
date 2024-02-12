# Rest Countries    

Rest Countries is a web application that provides information about different countries around the world. Users can explore details such as country names, flags, capitals, regions, populations, and languages spoken.       

# Table of Contents   
1. [Features](#Features)
1. [Usage](#Usage)
1. [Technologies Used](#Technologies-Used)
1. [Project Structure](#Project-Structure)
[]()

# Features    
- View details of various countries including flags, capitals, regions, populations, and languages.
- Access a modal window for detailed information about each country.
- Responsive design for seamless user experience across devices.   

# Usage   
1. Clone the repository:   
```git
git clone <repository-url>
```   
2. Open `index.html` in your web browser to launch the application.    

# Technologies Used    
1. HTML5 - `HTML-5`    
1. CSS3 - `CSS3`   
1. JavaScript - `JavaScript`   

# Project Structure   
- `index.html`: Main HTML file defining the structure of the web page.   
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rest Countries</title>
</head>
<body>
    <div class="container">
        <main>
            <div id="countries"></div>
            <div id="modal" class="modal">
                <div class="action-box">
                    <div id="icon-box" class="icon-box">
                        <span id="close" class="material-symbols-outlined">close</span>
                    </div>
                </div>
                <div class="modal-content">
                    <div id="modal-content"></div>
                    <div id="modal-flag" ></div>  
                </div>
                <div id="cancel-section">
                    <button id="btn-cancel"></button>
                </div>
                <div id="confirm-cancelation"></div>
            </div>
        </main>
    </div>
    <div class="container">
        <p > <span id="hr"></span> - <span id="min"></span> - <span id="sec"></span> - <span id="mili"></span></p>
    </div>
</body>
</html> 
```   
- `style.css`: CSS file containing styles for the application.   
```css

  @import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Ubuntu:wght@300;400;500;700&display=swap');

*{

}
html{

body{

}
img{

}


.container{

}
.container main{

}

 #countries{

}

#countries .country-card{

}

#countries .country-card .card-title{

}
#countries .country-card .card-title .country-count{

}
.card-flag {

}
#countries .country-card .card-flag img {

}
#countries .country-card .card-information{

}
#countries .country-card .card-information h2{

}
#countries .country-card .card-information .btn-btn{

}

#modal {

}
#modal .action-box{

}
#modal .action-box .icon-box #close{

}
#modal .modal-content{

}

#modal .modal-content #modal-content{

}
#modal .modal-content #modal-content h4 {

}
#modal .modal-content #modal-content p{


}
#modal .modal-content #modal-flag{

}


div#cancel-section {

}
button#btn-cancel {

}

#confirm-cancelation{

}
#confirm-text{

}
#confirm-cancelation #btn-container{

}
#confirm-cancelation #btn-container .btn {

}
.btn:nth-child(1){

}
.btn:nth-child(2){

}
```   
- `app.js`: JavaScript file implementing functionality for the Rest Countries application.   
