<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
</head>
<body>

<!-- Input fields for the first and second numbers -->
<p><label for="firstNumber">First Number:</label>
<input type="text" id="firstNumber" placeholder="Enter first number">
</p>
<p><label for="secondNumber">Second Number:</label>
<input type="text" id="secondNumber" placeholder="Enter second number">
</p>
<!-- Buttons for operations -->
<p><button onclick="performOperation('add')">Addition</button></p>
<p><button onclick="performOperation('subtract')">Subtraction</button></p>
<p><button onclick="performOperation('multiply')">Multiplication</button></p>
<p><button onclick="performOperation('divide')">Division</button></p>
<p><button onclick="performOperation('Result')">Result</button></p>

<!-- Result display area -->
<p id="result"></p>

<script>
    // Function to perform the selected operation
    function performOperation(operation) {
        // Get the input values
        var firstNumber = parseFloat(document.getElementById("firstNumber").value);
        var secondNumber = parseFloat(document.getElementById("secondNumber").value);

        // Check if both inputs are valid numbers
        if (isNaN(firstNumber) || isNaN(secondNumber)) {
            alert("Please enter valid numbers");
            return;
        }

        // Perform the selected operation
        var result;
        switch (operation) {
            case 'add':
                result = firstNumber + secondNumber;
                break;
            case 'subtract':
                result = firstNumber - secondNumber;
                break;
            case 'multiply':
                result = firstNumber * secondNumber;
                break;
            case 'divide':
                if (secondNumber !== 0) {
                    result = firstNumber / secondNumber;
                } else {
                    alert("Cannot divide by zero");
                    return;
                }
                break;
            default:
                alert("Invalid operation");
                return;
        }

        // Display the result
        document.getElementById("result").innerText = "Result: " + result;
    }
</script>

</body>
</html>
# javascript-calculator
we are using html and javascript for crating a calculator
