<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Circuitos de Compuertas Lógicas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .circuit {
            margin-bottom: 20px;
        }
        .circuit h2 {
            margin-bottom: 10px;
        }
        .led {
            width: 20px;
            height: 20px;
            background-color: grey;
            border-radius: 50%;
            display: inline-block;
            margin-left: 10px;
        }
    </style>
</head>
<body>
    <h1>Circuitos de Compuertas Lógicas</h1>

    <div class="circuit" id="and-circuit">
        <h2>Compuerta Lógica AND (IC 7408)</h2>
        <label>Interruptor A: <input type="checkbox" id="and-switch-a" onchange="updateAND()"></label>
        <label>Interruptor B: <input type="checkbox" id="and-switch-b" onchange="updateAND()"></label>
        <div>LED: <div class="led" id="and-led"></div></div>
    </div>

    <div class="circuit" id="or-circuit">
        <h2>Compuerta Lógica OR (IC 7432)</h2>
        <label>Interruptor A: <input type="checkbox" id="or-switch-a" onchange="updateOR()"></label>
        <label>Interruptor B: <input type="checkbox" id="or-switch-b" onchange="updateOR()"></label>
        <div>LED: <div class="led" id="or-led"></div></div>
    </div>

    <div class="circuit" id="not-circuit">
        <h2>Compuerta Lógica NOT (IC 7404)</h2>
        <label>Interruptor A: <input type="checkbox" id="not-switch-a" onchange="updateNOT()"></label>
        <div>LED: <div class="led" id="not-led"></div></div>
    </div>

    <script>
        function updateAND() {
            const a = document.getElementById('and-switch-a').checked;
            const b = document.getElementById('and-switch-b').checked;
            const led = document.getElementById('and-led');
            if (a && b) {
                led.style.backgroundColor = 'green';
            } else {
                led.style.backgroundColor = 'grey';
            }
        }

        function updateOR() {
            const a = document.getElementById('or-switch-a').checked;
            const b = document.getElementById('or-switch-b').checked;
            const led = document.getElementById('or-led');
            if (a || b) {
                led.style.backgroundColor = 'green';
            } else {
                led.style.backgroundColor = 'grey';
            }
        }

        function updateNOT() {
            const a = document.getElementById('not-switch-a').checked;
            const led = document.getElementById('not-led');
            if (!a) {
                led.style.backgroundColor = 'green';
            } else {
                led.style.backgroundColor = 'grey';
            }
        }
    </script>
</body>
</html>
