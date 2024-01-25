# pinpad1
<!DOCTYPE html> 
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>&#128513;my pinpad</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    #pin-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
    }

    .button {
      color: rgb(24, 61, 61);
      width: 60px;
      height: 60px;
      font-size: 30px;
      text-align: center;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div id="pin-container">
    <div class="button" onclick="appendToPin(1)">1</div>
    <div class="button" onclick="appendToPin(2)">2</div>
    <div class="button" onclick="appendToPin(3)">3</div>
    <div class="button" onclick="appendToPin(4)">4</div>
    <div class="button" onclick="appendToPin(5)">5</div>
    <div class="button" onclick="appendToPin(6)">6</div>
    <div class="button" onclick="appendToPin(7)">7</div>
    <div class="button" onclick="appendToPin(8)">8</div>
    <div class="button" onclick="appendToPin(9)">9</div>
    <div class="button" onclick="clearPin()">C</div>
    <div class="button" onclick="appendToPin(0)">0</div>
    <div class="button" onclick="submitPin()">Submit</div>
  </div>
  <p id="count">Pin: 0</p>
  <script>

    const correctPin = '1114'
    let enteredPin = '';


    function appendToPin(num) {
      enteredPin += num;
      document.getElementById('count').innerHTML=enteredPin;
    }


    function clearPin() {
      enteredPin = '';
      console.log('Pin Cleared');
    }

    function submitPin() {
      if (enteredPin === correctPin) {
        alert('Correct Pin! Initiating Action');
        // Add your desired action here, such as changing an image or text.
      } else {
        alert('Incorrect Pin. Try again.');
        clearPin();
      }
    }
  </script>
</body>
</html> 
