<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Mensagem Motivacional</title>
  <style>
    * {
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
    }

    body {
      height: 100vh;
      background: linear-gradient(-45deg, #ff9a9e, #fad0c4, #fbc2eb, #a1c4fd);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .card {
      background: rgba(255, 255, 255, 0.15);
      padding: 2.5rem;
      border-radius: 25px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      max-width: 450px;
      text-align: center;
      color: white;
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .message {
      font-size: 1.5rem;
      margin-bottom: 2rem;
      min-height: 70px;
      transition: opacity 0.5s ease;
    }

    button {
      padding: 1rem 2rem;
      background-color: rgba(255, 255, 255, 0.2);
      color: #fff;
      border: 2px solid white;
      border-radius: 50px;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s, transform 0.2s;
    }

    button:hover {
      background-color: rgba(255, 255, 255, 0.4);
      transform: scale(1.05);
    }

    /* Partículas decorativas */
    .particles {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }

    .particles span {
      position: absolute;
      display: block;
      width: 8px;
      height: 8px;
      background: rgba(255, 255, 255, 0.4);
      border-radius: 50%;
      animation: floatParticle 10s linear infinite;
      top: 100%;
    }

    @keyframes floatParticle {
      0% {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      100% {
        transform: translateY(-120vh) scale(0.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="particles">
    <!-- 20 partículas -->
    <span style="left: 10%; animation-delay: 0s;"></span>
    <span style="left: 25%; animation-delay: 2s;"></span>
    <span style="left: 40%; animation-delay: 4s;"></span>
    <span style="left: 55%; animation-delay: 6s;"></span>
    <span style="left: 70%; animation-delay: 1s;"></span>
    <span style="left: 85%; animation-delay: 3s;"></span>
    <span style="left: 15%; animation-delay: 5s;"></span>
    <span style="left: 30%; animation-delay: 7s;"></span>
    <span style="left: 45%; animation-delay: 2s;"></span>
    <span style="left: 60%; animation-delay: 8s;"></span>
    <span style="left: 75%; animation-delay: 4s;"></span>
    <span style="left: 90%; animation-delay: 6s;"></span>
    <span style="left: 20%; animation-delay: 1s;"></span>
    <span style="left: 35%; animation-delay: 3s;"></span>
    <span style="left: 50%; animation-delay: 5s;"></span>
    <span style="left: 65%; animation-delay: 7s;"></span>
    <span style="left: 80%; animation-delay: 9s;"></span>
    <span style="left: 95%; animation-delay: 0.5s;"></span>
    <span style="left: 5%; animation-delay: 2.5s;"></span>
    <span style="left: 88%; animation-delay: 1.8s;"></span>
  </div>

  <div class="card">
    <div class="message" id="message">
      Clique no botão para receber sua mensagem!
    </div>
    <button onclick="showMessage()">Nova Mensagem</button>
  </div>

  <script>
    const messages = [
      "Acredite em você — todos os dias!",
      "Grandes coisas levam tempo. Não desista.",
      "Você é capaz de realizar o que sonha.",
      "Seja luz, mesmo nos dias nublados.",
      "A força está em continuar, mesmo com medo.",
      "Hoje é o primeiro dia do resto da sua vitória.",
      "Permita-se brilhar. O mundo precisa da sua luz.",
      "O impossível só existe até alguém provar o contrário."
    ];

    function showMessage() {
      const msgElement = document.getElementById("message");
      msgElement.style.opacity = 0;

      setTimeout(() => {
        const randomIndex = Math.floor(Math.random() * messages.length);
        msgElement.textContent = messages[randomIndex];
        msgElement.style.opacity = 1;
      }, 500);
    }
  </script>

</body>
</html>

