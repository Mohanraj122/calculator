
 
 *********************************************** I'm develop a calculator with the languages are html,css,and javascript *****************************************************
 *********************************************** In this we can calculate the Simple addition,subtraction,multiplication and division. ***************************************
 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        center{
            color: rgb(236, 37, 37);
            font-family: 'Times New Roman', Times, serif;
        }
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height:100vh;
            margin: 0;
            background-color: #f3f3f3;
        }

        .calculator {
            background: #e9d6d6;
            border-radius: 100px;
            box-shadow: 0 4px 10px rgba(151, 28, 28, 0.2);
            padding: 30px;
            width: 310px;
        }

        .display {
            width: 100%;
            height: 50px;
            margin-bottom: 50px;
            text-align: right;
            font-size: 1.5rem;
            padding: 5px 1px;
            border: 1px solid #693535;
            border-radius: 60px;
            background: #f9f9f9;
        }

        .buttons {
            display:grid;
            grid-template-columns: repeat(4, 2fr);
            gap: 20px;
        }

        .button {
            background: #0072ed;
            color: #fff;
            border: none;
            border-radius: 20px;
            padding: 15px;
            font-size: 1rem;
            cursor: pointer;
            transition: background -0.3s;
        }

        .button:hover {
            background: #0056b3;
        }

        .button.clear {
            background: #dc3545;
        }

        .button.clear:hover {
            background: #df5b68;
        }

        .button.equal {
            background: #28a745;
            grid-column: span 2;
            border-radius: 50px;
        }

        .button.equal:hover {
            background: #14b039;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <center><h1><u>CALCULATOR</u></h1></center>
        <input type="text" class="display" id="display" disabled>
        <div class="buttons">
            <button class="button" onclick="appendValue('7')">7</button>
            <button class="button" onclick="appendValue('8')">8</button>
            <button class="button" onclick="appendValue('9')">9</button>
            <button class="button" onclick="appendValue('/')">/</button>

            <button class="button" onclick="appendValue('4')">4</button>
            <button class="button" onclick="appendValue('5')">5</button>
            <button class="button" onclick="appendValue('6')">6</button>
            <button class="button" onclick="appendValue('*')">*</button>

            <button class="button" onclick="appendValue('1')">1</button>
            <button class="button" onclick="appendValue('2')">2</button>
            <button class="button" onclick="appendValue('3')">3</button>
            <button class="button" onclick="appendValue('-')">-</button>

            <button class="button" onclick="appendValue('0')">0</button>
            <button class="button" onclick="appendValue('.')">.</button>
            <button class="button clear" onclick="clearDisplay()">C</button>
            <button class="button" onclick="appendValue('+')">+</button>
<br>
            <button class="button equal" onclick="calculate()">=</button>
        </div>
    </div>

    <script>
        const display = document.getElementById('display');

        function appendValue(value) {
            display.value += value;
        }

        function clearDisplay() {
            display.value = '';
        }

        function calculate() {
            try {
                display.value = eval(display.value);
            } catch {
                display.value = 'Error';
            }
        }
    </script>
</body>
</html>

