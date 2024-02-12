# Rest Countries    

Rest Countries is a web application that provides information about different countries around the world. Users can explore details such as country names, flags, capitals, regions, populations, and languages spoken.       

# Table of Contents   
1. [Features](#Features)
1. [Usage](#Usage)
1. [Technologies Used](#Technologies-Used)
1. [Project Structure](#Project-Structure)
1. [Acknowledgement](#Acknowledgement)
1. [LICENSE](#LICENSE)

## Features    
- View details of various countries including flags, capitals, regions, populations, and languages.
- Access a modal window for detailed information about each country.
- Responsive design for seamless user experience across devices.   

## Usage   
1. Clone the repository:   
```git
git clone <repository-url>
```   
2. Open `index.html` in your web browser to launch the application.    

## Technologies Used    
1. HTML5 - `HTML-5`    
1. CSS3 - `CSS3`   
1. JavaScript - `JavaScript`   

## Project Structure   
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
```js
    
// ** modal 
const modal = document.getElementById(`modal`);
const iconBox = document.getElementById('icon-box');
const modalContent =  document.getElementById('modal-content');
const modalFlag = document.getElementById('modal-flag');
const countryCard = document.querySelectorAll('.country-card');
const close = document.getElementById('close');
const cancelButton = document.getElementById('btn-cancel');
const cancelSection = document.getElementById('confirm-cancelation');
// ** data load....

const loadCountries = () => {

};

const displayCountries = (countries) => {

    });

    const btnAction = document.querySelectorAll('.btn-btn');
    btnAction.forEach((btn, index) => {
        btn.addEventListener(`click`, (e) => {
            e.preventDefault();

        });
    });
};


const getCountryHTML= (country, index) => {

    return `
        <div class="country-card">
            <div class="card-title">
                <h3 class="country-count">#${index+1}</h3>
            </div>
            <div class="card-flag">
            <img src="${country.flags.png}"/>
            </div>
            <div class="card-information">
                <h2>${country.name.common}</h2>
            </div> 
        </div>
    `

};



loadCountries();




const countryModal= (country) => {

    let languageNames = country.languages? Object.values(country.languages): [];

    modalContent.innerHTML = '';
    modalContent.innerHTML = `
        <h4>${country.name.common}</h4>
        <p>Official Name: ${country.name.official}</p>
        <p>Capital City: ${country.capital}</p>
        <p>Region: ${country.region}</p>
        <p>Subregion: ${country.subregion}</p>
        <p>Area : ${country.area} sq. km</p>
        <p>Population : ${country.population}</p>
        <p>Language : ${languageNames.length>0 ? languageNames.join(', '):'N/A'}</p>
    `
    modalFlag.innerHTML = `
        <div = "flag-modal">
            <img class="modal-image" src="${country.flags.png}">
        </div>
    `
};
// ** close modal
const closeModal = () => {
    close.addEventListener('click', (e) => {
        e.preventDefault()

    });
};
closeModal();
// ** cancel button
cancelButton.innerHTML = 'cancel';
cancelButton.addEventListener('click', (e) => {

})

let cancelElement = (element,className, idName, text ) => {

}

let text = cancelElement('h3', 'confirm-text', 'confirm-text', 'are you sure to Quit?');
let btnContainer = cancelElement('div','btn-container','btn-container','') ;
let okButton = cancelElement('button', 'btn', 'confirm-button','Ok');
let discardButton = cancelElement('button', 'btn', 'discard','Discard');

let buttons = [okButton,discardButton]
;[...buttons].forEach(button=>btnContainer.appendChild(button));

function appending(appendator, ...items) {
    let item = [...items];
    [...items].forEach(item=>appendator.appendChild(item));
}
appending(cancelSection, text,btnContainer);

// ** discard button
document.getElementById(`discard`).addEventListener('click',(e) => {
    e.preventDefault();
    document.getElementById('confirm-cancelation').style.display= 'none';
});
// ** ok button 
document.getElementById(`confirm-button`).addEventListener('click', (e) => {
    e.preventDefault();

})



// *** time

let hr = document.getElementById('hr');
let min = document.getElementById('min');
let sec = document.getElementById('sec');
let mili = document.getElementById('mili')


setInterval(() => {

    let currentTime = new Date();
    hr.innerText = (currentTime.getHours()<10?"0":"")+currentTime.getHours();
    min.innerText =( currentTime.getMinutes()<10?"0":" ")+currentTime.getMinutes();
    sec.innerText = (currentTime.getSeconds()<10?"0":" ")+currentTime.getSeconds();
    
},1000)
```       


## Acknowledgement   
Special Thanks To 'https://restcountries.com/v3.1/all' To Organise this API in Such a WAy.   
## LICENSE    


This project is licensed under the Mozilla Public License Version 2.0 (MPL-2.0).

© 2024 Md Rakibul Hasan

For details, please refer to the [LICENSE](LICENSE) file in the root of this repository.

The MPL-2.0 License is a permissive open-source license that allows you to freely use, modify, and distribute this software. By contributing to or using this project, you agree to the terms and conditions of the MPL-2.0 License.



