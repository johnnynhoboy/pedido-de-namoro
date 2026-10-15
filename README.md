<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quer namorar comigo?</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #ffccd5;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        h1 {
            color: #d81159;
            font-size: 24px;
            margin-bottom: 40px;
            padding: 0 20px;
        }
        .buttons {
            position: relative;
            width: 100%;
            height: 100px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        button {
            padding: 12px 24px;
            font-size: 18px;
            font-weight: bold;
            border: none;
            border-radius: 20px;
            cursor: pointer;
        }
        #sim {
            background-color: #38b000;
            color: white;
        }
        #nao {
            background-color: #d90429;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>Quer namorar comigo? ❤️</h1>
    <div class="buttons">
        <button id="sim" onclick="aceitou()">Sim</button>
        <button id="nao" onmouseover="foge()" ontouchstart="foge()">Não</button>
    </div>

    <script>
        function foge() {
            const botaoNao = document.getElementById('nao');
            const larguraJanela = window.innerWidth - 100;
            const alturaJanela = window.innerHeight - 100;
            const aleatorioX = Math.floor(Math.random() * larguraJanela);
            const aleatorioY = Math.floor(Math.random() * alturaJanela);
            botaoNao.style.left = aleatorioX + 'px';
            botaoNao.style.top = aleatorioY + 'px';
        }

        function aceitou() {
            alert('Eba! Agora estamos namorando! ❤️💍');
            document.body.innerHTML = '<h1 style="color: #d81159; font-size: 32px;">Sabia que você ia dizer sim! Te amo! ❤️</h1>';
        }
    </script>
</body>
</html>
