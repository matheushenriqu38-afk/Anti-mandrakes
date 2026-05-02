<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Arcana Team #Return</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #050505;
            font-family: 'Courier New', monospace;
            color: #eee;
        }

        /* Bolinhas vermelhas subindo */
        .bolhas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .bolha {
            position: absolute;
            bottom: -30px;
            background: #ff0000;
            border-radius: 50%;
            opacity: 0.4;
            animation: sobe 9s linear infinite;
        }

        @keyframes sobe {
            0% { transform: translateY(0); opacity: 0.4; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }

        header {
            background: #000000cc;
            backdrop-filter: blur(12px);
            position: fixed;
            width: 100%;
            top: 0;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            border-bottom: 2px solid red;
            z-index: 20;
        }

        .logo {
            font-size: 1.7rem;
            font-weight: bold;
            color: red;
        }

        .logo span { color: white; }

        .botoes-aba {
            display: flex;
            gap: 20px;
        }

        .aba-btn {
            background: transparent;
            border: none;
            color: #ddd;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            padding: 5px 10px;
        }

        .aba-btn:hover {
            color: red;
        }

        section {
            max-width: 1000px;
            margin: 100px auto 40px;
            background: rgba(0,0,0,0.7);
            padding: 35px;
            border-radius: 28px;
            position: relative;
            z-index: 5;
            backdrop-filter: blur(3px);
        }

        h1, h2 { color: red; margin-bottom: 20px; }

        .comandos-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 25px 0;
        }

        .cmd {
            background: #111;
            border-left: 3px solid red;
            padding: 8px 12px;
            font-size: 0.85rem;
        }

        .preco {
            background: red;
            color: black;
            display: inline-block;
            padding: 5px 12px;
            font-weight: bold;
            border-radius: 20px;
            margin: 15px 0;
        }

        button, .btn {
            background: red;
            border: none;
            color: black;
            padding: 8px 18px;
            margin: 12px 12px 0 0;
            border-radius: 40px;
            font-weight: bold;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
        }

        .btn-discord {
            background: #5865F2;
            color: white;
        }

        .social-link {
            background: #111;
            border: 1px solid red;
            padding: 8px 18px;
            border-radius: 40px;
            text-decoration: none;
            color: white;
            display: inline-block;
            margin: 8px 12px 0 0;
        }

        .pix-box {
            border: 1px solid red;
            background: #111;
            padding: 20px;
            border-radius: 20px;
            margin-top: 20px;
            display: none;
        }

        footer {
            text-align: center;
            padding: 25px;
            border-top: 1px solid #222;
            margin-top: 40px;
            position: relative;
            z-index: 5;
            background: #050505;
        }

        .hidden {
            display: none;
        }
    </style>
    <script src="https://cdn.jsdelivr.net/npm/qrcodejs@1.0.0/qrcode.min.js"></script>
</head>
<body>

<div class="bolhas" id="bolhas"></div>

<header>
    <div class="logo">ARCANA <span>#RETURN</span></div>
    <div class="botoes-aba">
        <button class="aba-btn" onclick="mostrarAba('home')">🏠 HOME</button>
        <button class="aba-btn" onclick="mostrarAba('servicos')">⚙️ SERVIÇOS</button>
        <button class="aba-btn" onclick="mostrarAba('contato')">📱 CONTATO</button>
    </div>
</header>

<!-- ========== HOME ========== -->
<section id="home" class="aba-conteudo">
    <h1>⚔️ ARCANA TEAM #RETURN</h1>
    <p><strong>Disciplina e Honra acima de tudo.</strong></p>
    <p>Segurança Ofensiva, Pentesting, Automação de Exploits.</p>
    <p>Projetos exclusivos e ferramentas próprias.</p>
</section>

<!-- ========== SERVIÇOS ========== -->
<section id="servicos" class="aba-conteudo hidden">
    <h2>🛠️ PACOTE DE FERRAMENTAS</h2>
    <div class="comandos-grid">
        <div class="cmd">!ddos &lt;url&gt; &lt;threads&gt;</div>
        <div class="cmd">!slowloris &lt;url&gt; &lt;threads&gt;</div>
        <div class="cmd">!deface &lt;url&gt;</div>
        <div class="cmd">!scanurl &lt;url&gt;</div>
        <div class="cmd">!backdoor &lt;url&gt;</div>
        <div class="cmd">!scan &lt;ip&gt;</div>
        <div class="cmd">!bruteforce &lt;ip&gt; &lt;user&gt;</div>
        <div class="cmd">!sqlmap &lt;url&gt;</div>
        <div class="cmd">!reverse &lt;ip&gt; &lt;porta&gt;</div>
        <div class="cmd">!keylogger</div>
        <div class="cmd">!extract</div>
        <div class="cmd">!persist</div>
        <div class="cmd">!wifi</div>
        <div class="cmd">!stresstest &lt;url&gt; &lt;threads&gt; &lt;duracao&gt;</div>
    </div>

    <div class="preco">💰 APENAS R$15,00 (acesso vitalício)</div>

    <button id="btnComprar">💳 COMPREI COM O DONO</button>
    <a href="https://discord.gg/b7hXYtwZhR" target="_blank" class="btn btn-discord">🎮 VÁ PARA O DISCORD DO ARCANA</a>

    <div id="pixInfo" class="pix-box">
        <p>🔐 Chave PIX (cópia e cola):</p>
        <p style="background:black; padding:10px;">018d0ec6-1118-4793-abad-6cef3303c9c3</p>
        <p>📲 QR Code:</p>
        <div id="qrcode"></div>
        <p>✅ Após pagar, entre em contato pelo <strong>Discord: matheusbmx.</strong> com comprovante.</p>
    </div>
</section>

<!-- ========== CONTATO ========== -->
<section id="contato" class="aba-conteudo hidden">
    <h2>📱 MINHAS REDES SOCIAIS</h2>
    <a href="https://discord.gg/b7hXYtwZhR" target="_blank" class="social-link">🎙️ Discord</a>
    <a href="https://www.instagram.com/usuario_banido_97283" target="_blank" class="social-link">📸 Instagram</a>
    <a href="https://www.tiktok.com/@usuario_banido_97283" target="_blank" class="social-link">📱 TikTok</a>
</section>

<footer>
    <p>Arcana Team #Return — Disciplina e Honra acima de tudo.</p>
    <p>🔴 ADQUIRA EM SERVIÇOS</p>
</footer>

<script>
    // Bolinhas vermelhas
    for (let i = 0; i < 55; i++) {
        let b = document.createElement('div');
        b.className = 'bolha';
        let s = Math.random() * 8 + 3;
        b.style.width = s + 'px';
        b.style.height = s + 'px';
        b.style.left = Math.random() * 100 + '%';
        b.style.animationDuration = Math.random() * 10 + 5 + 's';
        b.style.animationDelay = Math.random() * 12 + 's';
        document.getElementById('bolhas').appendChild(b);
    }

    // Sistema de abas
    function mostrarAba(abaId) {
        document.querySelectorAll('.aba-conteudo').forEach(section => {
            section.classList.add('hidden');
        });
        document.getElementById(abaId).classList.remove('hidden');
    }

    // Botão PIX
    const btn = document.getElementById('btnComprar');
    const pixDiv = document.getElementById('pixInfo');
    btn.addEventListener('click', () => {
        if (pixDiv.style.display === 'block') {
            pixDiv.style.display = 'none';
        } else {
            pixDiv.style.display = 'block';
            if (!document.getElementById('qrcode').innerHTML.trim()) {
                new QRCode(document.getElementById('qrcode'), {
                    text: '018d0ec6-1118-4793-abad-6cef3303c9c3',
                    width: 160,
                    height: 160
                });
            }
        }
    });

    // Inicia na aba HOME
    mostrarAba('home');
</script>
</body>
</html>