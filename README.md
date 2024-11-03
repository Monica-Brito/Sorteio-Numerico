# Sorteio-Numerico
 Esse programa é muito simples. O usuário coloca o numero inicial para sorteio, e coloca o máximo. Por exemplo: se for para fazer um cartão da mega sena, basta colocar o inicio que é 01 e o máximo que é o 60, pois a mega sena sorteia até o 60. Daí é só clicar em sortear  e repetir o sortear até a quantidade de apostas. Feito em HTML

#Código HTML
<!DOCTYPE html>
<html lang="pt-br">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Sorteio online</title>
      <link href="style.css" rel="stylesheet" type="text/css"/>
</head>
<body>
    <div class="container">
        <h1>Sorteio Numérico</h1>
    <p>Entre com o valor minimo <input type="number" name="minimo" id="minimo"></p>
    <p>Entre com o valor maximo <input type="number" name="maximo" id="maximo"></p>
    <button onclick="sorteio()">sortear</button>

    <h1 id="resultado"></h1>

    <script src="script.js"></script> 

    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>

    <footer>
        Desenvolvido por Monica Brito
    </footer>

    </div>
      
</body>

</html>

#Código Javascript
function sorteio(){
   const min = document.getElementById("minimo").value;
   const max = document.getElementById("maximo").value;
   
   let sort = Math.floor(Math.random()*Math.floor(max))

   while(sort<min){

      sort=Math.floor(Math.random()*Math.floor(max));
   }

   document.getElementById("resultado").innerHTML=sort;
}

#CSS
h1 {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    color: red;
    background-color: aqua;

    }

    body{
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 50vh;
    }

        body h1{
            border: #008;    
            }

        .container{
            max-width: 300px;
            min-height: 500px;
            border-radius: 20px 20px 20px 20px;
            border: 2px solid #008;
            padding: 5px;
            box-shadow: 0 4px 4px 0 rgba(red, green, blue, alpha);
            }
        footer{
            background-color: yellow;
        }

        
    

    

    
    

