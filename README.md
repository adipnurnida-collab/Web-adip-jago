<!DOCTYPE html>
<html>
<head>
  <title>Galaxy</title>

  <style>
    body {
      margin: 0;
      overflow: hidden;
      background: radial-gradient(circle, #000010, black);
    }

    h1 {
      position: absolute;
      width: 100%;
      text-align: center;
      top: 40%;
      color: white;
      font-family: sans-serif;
      letter-spacing: 5px;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px blue; }
      to { text-shadow: 0 0 25px purple; }
    }

    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: white;
      border-radius: 50%;
      animation: fall linear infinite;
    }

    @keyframes fall {
      from { transform: translateY(-10px); }
      to { transform: translateY(100vh); }
    }
  </style>
</head>

<body>

<h1>Adipkeren</h1>

<script>
for (let i = 0; i < 150; i++) {
  let star = document.createElement("div");
  star.className = "star";

  star.style.left = Math.random() * window.innerWidth + "px";
  star.style.top = Math.random() * window.innerHeight + "px";

  star.style.animationDuration = (Math.random() * 5 + 2) + "s";

  document.body.appendChild(star);
}
</script>

</body>
</html>
