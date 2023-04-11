# Calculator
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>calculator</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>

    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="calculator">
            <p>Calculator</p>
            <input type="text" placeholder="0" id="output-screen">
            <button onclick="Clear()">Cl</button>
            <button onclick="del()">DEL</button>
            <button onclick="display('%')">%</button>
            <button onclick="display('/')">/</button>
            <button onclick="display('7')">7</button>
            <button onclick="display('8')">8</button>
            <button onclick="display('9')">9</button>
            <button onclick="display('*')">*</button>
            <button onclick="display('4')">4</button> 
            <button onclick="display('5')">5</button>
            <button onclick="display('6')">6</button>
            <button onclick="display('-')">-</button>
            <button onclick="display('1')">1</button>
            <button onclick="display('2')">2</button>      
            <button onclick="display('3')">3</button>
            <button onclick="display('+')">+</button>
            <button onclick="display('.')">.</button>
            <button onclick="display('0')">0</button>
            <button onclick="calculate()" class="equal">=</button>

        </div>
    </div>
    <script >
        let outputScreen = document.getElementById("output-screen");

        function display(num){
            outputScreen.value += num;

        }
        function calculate(){
            try{
                outputScreen.value = eval(outputScreen.value);
            }
            catch(err)
            {
                alert("invalid")
            }
        }
        function Clear(){
            outputScreen.value="";

        }
        function del(){
            outputScreen.value = outputScreen.value.slice(0,-1);
        }
    </script>
</body>
</html>
