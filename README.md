# ColorChangeProject

index.HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <title>Color Changer App</title>
</head>
<body>
    <div class="container">
    <h1>Background Color Changer</h1>
    <p>Click the button to change the background color</p>
    <button id="changeBtn">Change Color</button>

    </div>
    
    <script src="script.js"></script>
</body>
</html>





SCRIPT.JS

//Select Button//
const btn =
document.getElementById("changeBtn");

//fucntion to generate random color
function getRandomColor() {
    const letters = "0123456789ABCDEF";
    let color = "#";
    for (let i = 0; i < 6; i++) {
        color +=
letters[Math.floor(Math.random() * 16)];


    }
    return color;

}


//Event listner to change background
btn.addEventListener("click", () => {
    document.body.style.background = 
    getRandomColor();

});




STYLE.CSS

/*General styles*/
body {
    margin: 0;
    padding: 0;
    font-family: 'poppins', sans-serif;
    text-align: center;
    background: linear-gradient(135deg, #ffecd2, #fcb69f);
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;

}

/*container box*/
.container {
    background: white;
    padding: 40px;
    border-radius: 20px;
    box-shadow: 0px 8px 20px rgba(0,0,0,0.2);
    width: 400px;
    transition: all 0.3 ease;
}

.container:hover {
    transform: scale(1.05);

}

/*title*/
h1 {
    color: #333;

}

/*Button styling*/
button {
    background: #ff6f61;
    color: white;
    border: none;
    padding: 12px 25px;
    border-radius: 8px;
    font-size: 28px;
    cursor: pointer;
    margin-top: 20px;
    transition: 0.3s;

}

button:over {
    background: #ff3d2e;
    transform:scale(1.1);


}



