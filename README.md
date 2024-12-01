<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="BananaCoin - La Memecoin Navideña Inspirada en el Meme del Plátano">
    <title>BananaCoin - La Memecoin Navideña</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #FFD700, #FF4500);
            color: #fff;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        header {
            text-align: center;
            padding: 50px;
            background: #ffdd00;
            color: #ff4500;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        header img {
            width: 200px;
        }
        header h1 {
            font-size: 2.8rem;
            margin: 20px 0;
        }
        section {
            padding: 30px 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }
        h2 {
            color: #FFD700;
            text-align: center;
        }
        p {
            font-size: 1.2rem;
            line-height: 1.6;
        }
        .cta-buttons a {
            display: inline-block;
            margin: 10px;
            padding: 10px 20px;
            background: #FFD700;
            color: #FF4500;
            text-decoration: none;
            border-radius: 5px;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }
        .cta-buttons a:hover {
            background: #ff4500;
            color: #fff;
            transform: scale(1.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #111;
            color: #fff;
        }
        #snowflakes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1000;
        }
        .snowflake {
            position: absolute;
            top: -10px;
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            opacity: 0.8;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0.5; }
        }
    </style>
</head>
<body>
    <header>
        <img src="URL_DE_TU_IMAGEN" alt="Logo de BananaCoin">
        <h1>BananaCoin</h1>
        <p>¡La Memecoin Navideña Inspirada en el Meme del Plátano!</p>
    </header>
    <section>
        <div class="container">
            <h2>Descripción</h2>
            <p>BananaCoin está basada en el icónico plátano viral de Maurizio Cattelan. Hemos transformado este símbolo cultural en una criptomoneda divertida y valiosa. ¡Únete a nuestra comunidad y sé parte de la tendencia más fresca y navideña del 2024!</p>
        </div>
    </section>
    <section>
        <div class="container">
            <h2>Cómo Comprar</h2>
            <p>Adquirir BananaCoin es muy fácil. Solo sigue los pasos siguientes:</p>
            <div class="cta-buttons">
                <a href="#" id="connectPhantom">Conecta Phantom Wallet</a>
                <a href="#" id="connectMetaMask">Conecta MetaMask</a>
                <a href="#" id="buyToken">Compra en PancakeSwap</a>
            </div>
        </div>
    </section>
    <footer>
        <p>&copy; 2024 BananaCoin. ¡Todos los derechos reservados!</p>
    </footer>
    <div id="snowflakes"></div>

    <script src="https://cdn.jsdelivr.net/npm/web3/dist/web3.min.js"></script>
    <script>
        const snowflakesContainer = document.getElementById('snowflakes');
        for (let i = 0; i < 50; i++) {
            const snowflake = document.createElement('div');
            snowflake.className = 'snowflake';
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
            snowflakesContainer.appendChild(snowflake);
        }

        const connectPhantom = document.getElementById('connectPhantom');
        const connectMetaMask = document.getElementById('connectMetaMask');
        const buyToken = document.getElementById('buyToken');

        connectMetaMask.addEventListener('click', async () => {
            if (window.ethereum) {
                try {
                    await window.ethereum.request({ method: 'eth_requestAccounts' });
                    alert('MetaMask conectada.');
                } catch (error) {
                    alert('Error conectando MetaMask: ' + error.message);
                }
            } else {
                alert('MetaMask no está instalada.');
            }
        });

        buyToken.addEventListener('click', () => {
            window.location.href = 'https://pancakeswap.finance/';
        });
    </script>
</body>
</html>
