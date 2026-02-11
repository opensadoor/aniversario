
<html lang="pt-br">
<head>
    
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap');

        /* RESET BÁSICO */
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            /* Fundo Gradiente Roxo/Rosa */
            background: linear-gradient(-45deg, #c471ed, #f64f59, #12c2e9);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Poppins', sans-serif;
            overflow-y: auto; /* Rolagem liberada */
        }

        /* CONTAINER PRINCIPAL */
        .container {
            position: relative;
            z-index: 1000;
            width: 100%;
            max-width: 600px;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        /* ESTILO DO CARTÃO DE VIDRO */
        .glass-card {
            background: rgba(255, 255, 255, 0.25);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 2px solid rgba(255, 255, 255, 0.4);
            border-radius: 25px;
            padding: 2.5rem;
            text-align: center;
            color: #fff;
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
            width: 100%;
            animation: surgir 1s ease-out;
        }

        /* BOTÃO */
        .btn-open {
            background: #fff;
            color: #d6336c;
            border: none;
            padding: 15px 40px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.2s, background 0.2s;
            font-family: 'Poppins', sans-serif;
            animation: pulsar 2s infinite;
            pointer-events: auto; 
            position: relative;
            z-index: 1001;
        }

        .btn-open:hover {
            transform: scale(1.05);
            background: #ffe0e9;
        }

        .btn-open:active {
            transform: scale(0.95);
        }

        /* TEXTOS */
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.2rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
        }

        p {
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 15px;
            text-shadow: 0 1px 2px rgba(0,0,0,0.1);
        }

        .destaque {
            font-weight: 600;
            display: block;
            margin-top: 20px;
            font-size: 1.4rem;
            color: #ffe6fa;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }

        /* CONTROLE DE TELAS */
        #message-card { display: none; }
        #intro-card { display: block; }

        /* ANIMAÇÕES */
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes pulsar {
            0% { box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(255, 255, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(255, 255, 255, 0); }
        }

        @keyframes surgir {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsividade */
        @media (max-width: 600px) {
            h1 { font-size: 2.5rem; }
            .glass-card { padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <audio id="minhaMusica" loop>
        <source src="planos.mp3" type="audio/mpeg">
    </audio>

    <div class="container">
        
        <div id="intro-card" class="glass-card">
            <h1>Para você... ✨</h1>
            <p>Hoje é um dia especial e eu guardei algumas palavras.</p>
            
            <button id="botaoLer" class="btn-open" onclick="abrirCarta()">Ler Mensagem 💌</button>
        </div>

        <div id="message-card" class="glass-card">
            <h1>Feliz aniversário ✨🎂</h1>
            
            <p>Que esse novo ano venha leve, intenso e cheio de coisas boas acontecendo no tempo certo. Você merece tudo aquilo que faz o coração sorrir de verdade.</p>
            
            <p>Tem uma frase do Charlie Brown Jr. que sempre me lembra você: “O impossível é só questão de opinião.” E acho que é isso… porque desde que você chegou, muita coisa que parecia improvável começou a fazer sentido.</p>
            
            <p>Seu jeito, seu sorriso e sua presença têm algo que prende, que aproxima, que deixa vontade de ficar. Que hoje você se sinta especial — e que eu possa continuar fazendo parte dos seus dias, mesmo que aos poucos. 💫❤️</p>
            
            <p>Aproveita seu dia. Você é incrível.</p>

            <span class="destaque">Eu te amo menina❤️</span>
        </div>

    </div>

    <script>
        function abrirCarta() {
            var intro = document.getElementById('intro-card');
            var msg = document.getElementById('message-card');
            var musica = document.getElementById('minhaMusica');
            
            // Troca as telas
            intro.style.display = 'none';
            msg.style.display = 'block';
            
            // Rola a tela para o topo
            window.scrollTo({ top: 0, behavior: 'smooth' });

            
            }
        
    </script>

</body>
</html>

<audio id="midia" loop>
    <source src="planos.mp3" type="audio/mpeg">
</audio scr="midia/planos.mp3"controls autoplay auto></audio>
# aniversario
