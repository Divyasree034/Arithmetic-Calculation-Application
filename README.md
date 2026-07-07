<!DOCTYPE html>
<html>
<head>
  <title>Arithmetic Operations</title>
</head>
<body>
  <h2>Calculate Application</h2>
  
  <input type="number" id="num1" placeholder="Enter number 1">
  <input type="number" id="num2" placeholder="Enter number 2"><br><br>
  
  <select id="operation">
    <option value="add">Addition (+)</option>
    <option value="sub">Subtraction (-)</option>
    <option value="mul">Multiplication (×)</option>
    <option value="div">Division (÷)</option>
  </select><br><br>
  
  <button onclick="calculate()">Calculate</button><br><br>
  
  <input type="text" id="result" placeholder="Result" readonly>
  
  <script>
    function calculate() {
      var n1 = parseFloat(document.getElementById("num1").value);
      var n2 = parseFloat(document.getElementById("num2").value);
      var op = document.getElementById("operation").value;
      var res = "";

      if (isNaN(n1) || isNaN(n2)) {
        res = "Enter valid numbers";
      } else {
        if (op === "add") res = n1 + n2;
        else if (op === "sub") res = n1 - n2;
        else if (op === "mul") res = n1 * n2;
        else if (op === "div") {
          res = n2 !== 0 ? (n1 / n2) : "Cannot divide by zero";
        }
      }
      document.getElementById("result").value = res;
    }
  </script>
</body>
</html>
