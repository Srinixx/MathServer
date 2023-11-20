# Ex.05 Design a Website for Server Side Processing
## Date: 04/10/23

## AIM:
To design a website to find total surface area of a square prism in server side.

## FORMULA:
Total Surface Area = 2b<sup>2</sup> + 4bh
<br>b --> Base of Square Prism
<br>h --> Height of Square Prism

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        h1{
            text-align: center;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        }

        #calculator-container {
            background-color: #c18484;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(223, 16, 16, 0.2);
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin: 5px;
            color:black; 
            border-radius: 10px;
        }

        table {
            margin-top: 20px;
        }

        button {
            padding: 30px;
            font-size: 20px;
        }

        /* Define colors for operators */
        button[data-operator="+"] {
            background-color:rgb(70, 159, 201);
        }

        button[data-operator="-"] {
            background-color: rgb(70, 159, 201);
        }

        button[data-operator="*"] {
            background-color: rgb(70, 159, 201);
        }

        button[data-operator="/"] {
            background-color: rgb(70, 159, 201);
        }

        button[data-operator="%"] {
            background-color:rgb(70, 159, 201);
        }

        button[data-operator="sqrt"] {
            background-color: rgb(70, 159, 201);
        }
    </style>
</head>
<body>
    <div id="calculator-container">
        <h1>CALCULATOR</h1>
        <input type="text" id="display" readonly>
        <table>
            <tr>
                <td><button onclick="appendToDisplay('1')" style="color: rgb(204, 17, 17);">1</button></td>
                <td><button onclick="appendToDisplay('2')" style="color: rgb(204, 17, 17);">2</button></td>
                <td><button onclick="appendToDisplay('3')" style="color: rgb(204, 17, 17);">3</button></td>
                <td><button data-operator="+" onclick="appendToDisplay('+')" style="color: white;">+</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('4')" style="color: rgb(204, 17, 17);">4</button></td>
                <td><button onclick="appendToDisplay('5')" style="color: rgb(204, 17, 17);">5</button></td>
                <td><button onclick="appendToDisplay('6')" style="color: rgb(204, 17, 17);">6</button></td>
                <td><button data-operator="-" onclick="appendToDisplay('-')" style="color: white;">-</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('7')" style="color: rgb(204, 17, 17);">7</button></td>
                <td><button onclick="appendToDisplay('8')" style="color: rgb(204, 17, 17);">8</button></td>
                <td><button onclick="appendToDisplay('9')" style="color: rgb(204, 17, 17);">9</button></td>
                <td><button data-operator="*" onclick="appendToDisplay('*')" style="color: white;">*</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('0')" style="color: rgb(204, 17, 17);">0</button></td>
                <td><button data-operator="%" onclick="appendToDisplay('%')" style="color: rgb(222, 208, 208);">%</button></td>
                <td><button data-operator="sqrt" onclick="calculateSquareRoot()" style="color: rgb(224, 209, 209);">^</button></td>
                <td><button data-operator="/" onclick="appendToDisplay('/')" style="color: rgb(237, 231, 231);">/</button></td>
            </tr>
            <tr>
                <td><button onclick="clearDisplay()">C</button></td>
                <td><button onclick="appendToDisplay('.')">.</button></td>
                <td><button onclick="appendToDisplay('00')">00</button></td>
                <td><button onclick="calculateResult()" style="color: rgb(20, 155, 25);">=</button></td>
            </tr>
        </table>
    </div>
    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculateResult() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }

        function calculateSquareRoot() {
            const inputValue = document.getElementById('display').value;
            const result = Math.sqrt(parseFloat(inputValue));
            document.getElementById('display').value = result;
        }
    </script>
</body>
</html>
```
## OUTPUT:
 ![image](https://github.com/Srinixx/MathServer/assets/132982592/05ca52fc-7e61-4b3b-9f9c-ae7b196c1ed5)

 ![image](https://github.com/Srinixx/MathServer/assets/132982592/b6df6d1a-89d7-4582-9962-d680151fb090)




## RESULT:
The program for performing server side processing is completed successfully.
