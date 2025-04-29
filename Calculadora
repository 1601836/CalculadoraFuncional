<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: sans-serif;
        }
        body{
            min-height: 100vh;
            background-color: black;
            display: grid;
            place-items: center;
        }
        .calculadora{
            background-color: rgb(40, 40, 80);
            color: white;
            width: 350px;
            max-width: 100% ;
            padding: 1.5rem;
            border-radius: 1rem;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: .5rem;
        }
        .pantalla{
            grid-column: 1/-1;
            background-color: black;
            padding: 1.5rem;
            font-size: 2rem;
            text-align: right;
            border-radius: .5rem;
            margin-bottom: 1rem;
            font-family: monospace;
            font-weight: 600;
        }
        .btn{
            background-color:black;
            color: white;
            border: 0;
            padding: 1.5rem .5rem;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: .5rem;
            cursor: pointer;
            font-weight: 900;
        }
        .btn:hover{
            background-color: beige;
            color: black;
            font-weight: 900;
        }
        #cero{
            grid-column: span 2;
        }
        #igual{
            grid-row: span 2;
            background-color: red;
        }
        #igual:hover{
            background-color: beige;
        }

    </style>
</head>
<body>
    
    <div class="calculadora">
        <div class="pantalla">0</div>
            <button id="c" class="btn">C</button>
            <button id="borrar" class="btn">←</button>
            <button class="btn">/</button>
            <button class="btn">*</button>
            <button class="btn">7</button>
            <button class="btn">8</button>
            <button class="btn">9</button>
            <button class="btn">-</button>
            <button class="btn">4</button>
            <button class="btn">5</button>
            <button class="btn">6</button>
            <button class="btn">+</button>
            <button class="btn">1</button>
            <button class="btn">2</button>
            <button class="btn">3</button>
            <button id="igual" class="btn">=</button>
            <button id="cero" class="btn">0</button>
            <button class="btn">.</button>      
    </div>

    <script>
        const pantalla = document.querySelector(".pantalla");
        const botones = document.querySelectorAll(".btn");

        botones.forEach(boton => {
            boton.addEventListener("click", () => {
                const botonApretado = boton.textContent;

                if(boton.id === "c"){
                    pantalla.textContent = "0";
                    return;
                }

                if(boton.id === "borrar"){
                    if(pantalla.textContent.length === 1 || pantalla.textContent === "Error!"){
                        pantalla.textContent = "0";
                    } else {
                        pantalla.textContent = pantalla.textContent.slice(0,-1);                     
                    }
                    return; 
                }

                if(boton.id === "igual"){
                    try{
                        pantalla.textContent = eval(pantalla.textContent);
                    } catch {
                        pantalla.textContent = "Error!";
                    }            
                    return;
                }

                if(pantalla.textContent === "0" || pantalla.textContent === "Error!"){
                    pantalla.textContent = botonApretado;
                } else{
                    pantalla.textContent += botonApretado;
                }
            })
        })
    </script>
</body>
</html>
