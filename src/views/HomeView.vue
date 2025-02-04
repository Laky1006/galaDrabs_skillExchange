<template>
  
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>

</head>
<body>
    <header>
        <nav id = "nav-desktop">

            <div id = "nav-div">
                <a href="HomeView.vue" class="nav-option">Home</a>
                <a href="HomeView.vue" class = "nav-option">About</a>

                <div class="dropdown">

                    <a href="HomeView.vue" class="dropbtn nav-option">Contacts</a>
                    <div class="dropdown-content">
                      <a href="#">These</a>
                      <a href="#">Do Nothing</a>
                      <a href="#">For now</a>
                    </div>

                </div>
            </div>

        </nav>

        <nav class="nav-mobile">
            <a class="active">More info</a>
            <div id="myLinks">
                <a href="HomeView.vue" class="nav-option-mobile">Home</a>
                <a href="HomeView.vue" class = "nav-option-mobile">About</a>
                <a href="HomeView.vue" class="nav-option-mobile">Contacts</a>
            </div>
            <a href="javascript:void(0);" class="icon" onclick="myFunction()">
                <span id = "menu-icon">&Xi;</span>
            </a>
        </nav>
    </header>

    <main>
 
        <h1>Atrodi savu privātskoltāju</h1> 


        <section>
            <div id="kartites-section">

                <div class = "kartite">
                    <img src="https://cdn.prod.website-files.com/62d84e447b4f9e7263d31e94/637627ca9eebde45ae5f394c_Underwater-Nun.jpeg" class = "kartite-img">
                    <h2>Peldēšanas nodarbība</h2>
                    <p>Mācies peldēt kopā!</p>
                    <button class="button-kartites" id="eepy-cat-btn">Pieteikties stundai</button>
                </div>

                <div class = "kartite">
                    <img src="https://brandingforthepeople.com/wp-content/uploads/2019/04/Stock-Photography-vs-Real-Imagery.jpg" class = "kartite-img">
                    <h2>Matemātikas nodarbības ar Jāni</h2>
                    <p>Atpaliec skolā un nesaproti algebru? Nāc mācīties!</p>
                    <button class="button-kartites" id="orange-btn">Pieteikties stundai</button>
                </div>

                <div class = "kartite">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRq2WR9_mQ1Scq73egekcYoT2qj7Bt2crFk2w&s" class = "kartite-img">
                    <h2>Desertu pagatavošana</h2>
                    <p>Iemācies gatavot desertus kā īsts šefvpavārs</p>
                    
                    <button class="button-kartites" id="wizard-btn">Pieteikties stundai</button>
                </div>
                
            </div>

        </section>
    </main>

            
</body>
</html>

</template>


<!-- <script>
  export default {
    data(){
      return {
        score: 0,
      }
    },
    methods: {
      handleClickEvent(){
        this.score++
      }
    }
  }
</script> -->

<script>

    function darkModeFunction() {
        // var element = document.body;
        // element.classList.toggle("dark-mode");

        alert("it works");
    }

    function myFunction() {
        var x = document.getElementById("myLinks");
        if (x.style.display === "block") {
            x.style.display = "none";
        } else {
            x.style.display = "block";
        }
    }


</script>


<style scoped>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #edfaeb;
    font-family: sans-serif;
    color: #043811;
}

header {
    background-image: linear-gradient(#439b43, #88e984, #439b43);
    padding: 10px 10px 10px 10px;
}

main {
    line-height: 1.6;
    height: 100%;
    width: 100%;
    padding: 10px 30px 30px 30px;
}

#nav-desktop {
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;

}

#nav-div {
    width: 35%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 0px 30px 0px 30px;
}

#nav-desktop p {
    color: #d6fcd6;
    font-size: 35px;
    font-weight: bolder;
    text-decoration: none;
}

.nav-option {
    color: #d6fcd8;
    font-family: 'Courier New', Courier, monospace;
    font-size: 35px;
    font-weight: bolder;
    text-decoration: none;
    text-shadow: 0px 1px 5px #0e3506;

}

.nav-option:hover {
    color: #f7f7f7;
    text-shadow: 0px 4px 7px #17a323;
}

.dropdown {
    margin: 0;
}

.dropbtn {   
    margin: 0;
}

/* Dropdown content (hidden by default) */
.dropdown-content {
    display: none;
    position: absolute;
    top: 70px;
    background-color: #d5fad8;
    width: 200px;
    box-shadow: 0px 8px 16px #81b484;
    z-index: 1;
}
  
.dropdown-content a {
    float: none;
    color: #0b7407;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    text-align: left;
}

.dropdown-content a:hover {
    background-color: #93f098;
}
  
/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
    display: block;
}

section {
    margin-top: 30px;
}

.img-section {
    width: 100px;
    height: auto;
}

#kartites-section {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    row-gap: 30px;
    flex-wrap: wrap;
}

.section-div {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.kartite-img {
    height: 300px;
    width: 300px;
}

.kartite {
    height: 500px;
    width: 500px;
    padding: 5px;
    margin: 5px;
    background-color: #b5e9b3;
    border: solid;
    border-color: #3f5c40;
    border-width: 2px;
    border-radius: 10px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

@keyframes example {
    0% {
        transform: translateY(0);
    }

    100% {
        transform: translateY(-15px);
        box-shadow: -5px 5px 10px #365a3f;
    }


    
}

.kartite:hover {
    animation: example 2s;
    
}

.button-kartites {
    background-color: #2a8837;
    border-radius: 7px;
    border-color: #077407;
    padding: 4px;
    margin: 10px;
    color: aliceblue;
    font-weight: bold;
    
}

.button-kartites:hover {
    background-color: #055709;
    padding: 6px;
    margin: 8px;
}


/* The Modal (background) */
.modal {
    display: none;
    position: fixed; 
    z-index: 1; 
    left: 0;
    top: 0;
    width: 100%; 
    height: 100%; 
    overflow: auto; 
    background-color: rgba(0,0,0,0.4); 
}
  
  /* Modal Content/Box */
.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    width: 80%; /* Could be more or less, depending on screen size */
}
  
  /* The Close Button */
.close {
    color: #696969;
    float: right;
    font-size: 28px;
    font-weight: bold;
}
  
.close:hover,
.close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.nav-mobile {
    display: none;
    overflow: hidden;
    background-color: #fad5f2;
    position: relative;
}

.nav-mobile #myLinks {
    display: none;
}

.nav-mobile a {
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
    display: block;
}

.nav-mobile span {
    color: #fdedfb;
}

.nav-mobile a.icon {
    background: #570331;
    display: block;
    position: absolute;
    right: 0;
    top: 0;
}

.nav-mobile a.icon:hover {
    background: #81054a;
}

.nav-option-mobile {
    color: #5c0a47;
}

.nav-option-mobile:hover {
    background-color: #e79fd8;
    color: #5c0a47;
}

.active {
    background-color: #bd1886;
    color: #fdedfb;
}

@media (max-width: 1600px) and (min-width: 1300px) {
    .kartite {
        height: 400px;
        width: 400px;
    }

    .kartite-img {
        height: 250px;
    }

}

@media (max-width: 1300px) and (min-width: 1050px){
    
    #nav-desktop p {
        font-size: 28px;
    }
    
    .nav-option {
        font-size: 28px;    
    }
    
    .kartite {
        height: 300px;
        width: 300px;
    }

    .kartite-img {
        height: 170px;
    }

    .kartite h2 {
        font-size: 18px;
    }

    .kartite p {
        font-size: 13px;
    }

    .button-kartites {
        padding: 3px;
        margin: 5px;
        font-size: 13px; 
    }

    .button-kartites:hover {
        background-color: #0c8508;
        padding: 5px;
        margin: 3px;
    }
}

@media (max-width: 1050px) and (min-width: 875px){

    #nav-desktop p {
        font-size: 25px;
    }
    
    .nav-option {
        font-size: 28px;    
    }

    .kartite {
        height: 400px;
        width: 400px;
    }

    .kartite-img {
        height: 250px;
    }

}

@media (max-width: 875px) {

    #nav-desktop{
        display: none;
    }

    .nav-mobile {
        display: block;
    }

    #kartites-section {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
}

@media (max-width: 550px){

    .kartite {
        height: 300px;
        width: 300px;
    }

    .kartite-img {
        height: 170px;
    }

    .kartite h2 {
        font-size: 18px;
    }

    .kartite p {
        font-size: 13px;
    }

    .button-kartites {
        padding: 3px;
        margin: 5px;
        font-size: 13px; 
    }

    .button-kartites:hover {
        background-color: #088508;
        padding: 5px;
        margin: 3px;
    }
}

</style>