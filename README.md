Calculadora


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        *{
            margin: 0%;
            padding: 0%;
        }
        .fundo{
            
            background-image: linear-gradient(45deg, black, purple);
            height: 100vh;
            color: white;
            font-family: Arial, Helvetica, sans-serif;
            text-align: center;
        }
        .calculadora{

            position: absolute;
            background-color: rgba(0, 0, 0, 0.7);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 15px;
            padding: 15px;

        }

        .bt{
            width: 50px;
            height: 50px;
            font-size: 25px;
            cursor: pointer;
            background-color: rgb(31, 31, 31);
            border: none;
            color:rgb(236, 235, 233);
            margin: 3px;
        }
        .bt:hover{
            background-color: black;
        }

        #resultado{
            background-color: aliceblue;
            width: 207px;
            height: 30px;
            margin: 6px;
            font-size: 25px;
            color: black;
            text-align: right;

        }
    </style>
</head>
<body>
    <div class="fundo">
        <H1>Angela Vidal</H1>

        <div class="calculadora">
            <h1>Calculadora</h1>
            <p id="resultado"> </p>
            <table>
                <tr><button class="bt"onclick="clean( )">C</button></tr>
                <tr><button class="bt"onclick="back('&lt')">&lt</button></tr>
                <tr><button class="bt"onclick="insert( '÷' )">÷</button></tr>
                <tr><button class="bt"onclick="insert('X')">X</button></tr>
            </table>
            <table>
                <tr><button class="bt" onclick="insert('7')">7</button></tr>
                <tr><button class="bt" onclick="insert('8')">8</button></tr>
                <tr><button class="bt" onclick="insert('9')">9</button></tr>
                <tr><button class="bt"onclick="insert('-')"> -</button></tr>
            </table>
            <table>
                <tr><button class="bt" onclick="insert('4')">4</button></tr>
                <tr><button class="bt" onclick="insert('5')">5</button></tr>
                <tr><button class="bt" onclick="insert('6')">6</button></tr>
                <tr><button class="bt"onclick="insert('+')">+</button></tr>
            </table>
            <table>
                <tr><button class="bt" onclick="insert('1')">1</button></tr>
                <tr><button class="bt" onclick="insert('2')">2</button></tr>
                <tr><button class="bt" onclick="insert('3')">3</button></tr>
                <tr aria-rowspan="2" ><button class="bt" style="height: 53px;" onclick="calcular('=')">=</button></tr>
            </table>
            <table>
                <tr aria-colspan="2"><button class="bt" style="width: 106px;" onclick="insert('0')">0</button></tr>
                <tr><button class="bt"onclick="insert('.')">.</button></tr>
            </table>
        </div>
    </div>
    <script>
        function insert(num)
        {

           var numero = document.getElementById('resultado').innerHTML;
           document.getElementById('resultado').innerHTML = numero + num;
            
        }

        function clean ()
        {
            document.getElementById('resultado').innerHTML = "";
        }

        function back ()
        {
           var resultado = document.getElementById('resultado').innerHTML;
           document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1);
        }

        function calcular ()
        {
            var resultado = document.getElementById('resultado').innerHTML;
            if(resultado)
        {
            document.getElementById('resultado').innerHTML = eval(resultado);
        }
        }


    </script>
    
</body>
</html>
