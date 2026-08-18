[index.html](https://github.com/user-attachments/files/31164499/index.html)
<!doctype html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <title>Pertanyaan Penting</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: grid;
      place-items: center;
      font-family: Arial, sans-serif;
      background: #ffe6ef;
      overflow: hidden;
    }

    .card {
      text-align: center;
      background: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 8px 25px #0002;
    }

    button {
      border: 0;
      border-radius: 10px;
      padding: 12px 24px;
      margin: 10px;
      font-size: 18px;
      cursor: pointer;
    }

    #iya { background: #ff4f87; color: white; }
    #tidak {
      background: #ddd;
      position: fixed;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Maukan kamu jadi temenku ? 🥺</h1>
    <button id="iya">Mau!</button>
    <button id="tidak">Tidak</button>
  </div>

  <script>
    const tidak = document.getElementById("tidak");

    function pindahTombol() {
      const x = Math.random() * (window.innerWidth - tidak.offsetWidth);
      const y = Math.random() * (window.innerHeight - tidak.offsetHeight);

      tidak.style.left = `${x}px`;
      tidak.style.top = `${y}px`;
    }

    tidak.addEventListener("mouseenter", pindahTombol);
    tidak.addEventListener("click", pindahTombol);

    document.getElementById("iya").addEventListener("click", () => {
      document.body.innerHTML = "<h1>Yeay, Thank YOUU! 🎉🎉🎉🎉</h1>";
    });
  </script>
</body>
</html>
