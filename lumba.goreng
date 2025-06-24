<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>BNG VLAN Generator</title>
  <style>
    body {
      font-family: sans-serif;
      padding: 20px;
      max-width: 700px;
      margin: auto;
    }
    textarea {
      width: 100%;
      height: 150px;
      margin-bottom: 10px;
      font-family: monospace;
    }
    button {
      padding: 10px 20px;
      font-weight: bold;
      background: #0069d9;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background: #0053b3;
    }
  </style>
</head>
<body>
  <h2>BNG VLAN Generator</h2>
  <p>2510,2511,2512:</p>
  <textarea id="input" placeholder="2510,2511,2512"></textarea>
  <button onclick="generate()">Generate</button>
  <h3>Hasil Output:</h3>
  <textarea id="output" readonly></textarea>

  <script>
    function generate() {
      const input = document.getElementById("input").value;
      const vlans = input.split(/[\s,]+/).filter(v => v !== '');
      let output = vlans.map(vlan => `service-port vlan ${vlan} gpon 0/1/1 ont 1 gemport 1 multi-service user-vlan ${vlan}`).join('\n');
      document.getElementById("output").value = output;
    }
  </script>
</body>
</html>
