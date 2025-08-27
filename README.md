[Nah, I'd win.html](https://github.com/user-attachments/files/22013203/Nah.I.d.win.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Kesley Cakes</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
    --bg:#0045f5;
    --muted:#141821;
    --text:#e6e8ee;
    --sub:#ffffff;
    --brand:#6b8cff;
    --brand-2:#7ef0d1;
    --stroke:#232838;
    --radius:20px;
    --shadow:0 10px 30px rgba(0,0,0,.35);
    --pix-color: #4b2c20;
}
*{box-sizing:border-box;margin:0;padding:0}
body {
    font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,'Helvetica Neue',Arial,sans-serif;
    color:var(--text);
    background:radial-gradient(1200px 800px at 80% -10%, rgba(107,140,255,.15), transparent 60%),
               radial-gradient(1000px 700px at -10% 10%, rgba(126,240,209,.12), transparent 60%),
               var(--bg);
    line-height:1.6;
}
a{color:inherit;text-decoration:none}
img{max-width:100%;display:block}
.container{max-width:1200px;margin:0 auto;padding:0 20px}

header {
    position:sticky;top:0;z-index:50;
    backdrop-filter:saturate(140%) blur(8px);
    background:rgba(11,13,18,.6);
    border-bottom:1px solid var(--stroke);
}
.nav{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
.logo{display:flex;gap:10px;align-items:center;font-weight:800;letter-spacing:.3px}
.logo-badge{width:28px;height:28px;border-radius:8px;background:linear-gradient(135deg,var(--brand),var(--brand-2));box-shadow:var(--shadow)}
.nav-links{display:flex;gap:20px;align-items:center}

.btn {
    display:inline-flex;align-items:center;justify-content:center;gap:8px;
    padding:10px 16px;border-radius:12px;border:1px solid var(--stroke);
    background:rgba(255,255,255,.03);font-weight:600;cursor:pointer;
    transition:all .3s ease-in-out;
    position: relative;overflow: hidden;
}
.btn.primary {
    background: linear-gradient(135deg, var(--brand), var(--brand-2));
    color:#0b0d12;border-color:transparent;
    box-shadow: 0 0 15px var(--brand-2), inset 0 0 10px rgba(255,255,255,0.2);
}
.btn:hover, .btn.primary:hover, .card button:hover {opacity:0.85; transform: scale(1.08); box-shadow:0 0 25px var(--brand-2);}
.btn:active, .btn.primary:active, .card button:active {transform: scale(0.95); box-shadow:0 0 10px var(--brand);}

/* LOGIN PAGE */
#login-page {
    display:flex;flex-direction:column;align-items:center;justify-content:center;
    height:100vh;text-align:center;padding:20px;
}
#login-box {
    background:var(--muted);padding:40px 30px;border-radius:var(--radius);
    box-shadow:var(--shadow);max-width:400px;width:100%;
}
#login-box h1 {margin-bottom:20px;font-size:1.8rem}
#login-box .btn {width:100%}

/* STORE CONTENT */
.banner {
    padding:80px 20px;text-align:center;margin-top:20px;
    border-radius:var(--radius);
    background:linear-gradient(135deg,var(--brand),var(--brand-2));
    color:#0b0d12;
}
.banner h1 {font-size:2.5rem;margin-bottom:10px}
.banner p {font-size:1.2rem;color:#0b0d12;opacity:0.85}

.produtos {padding:50px 0}
.produtos h2 {font-size:2rem;margin-bottom:30px;text-align:center}
.card-container {
    display:grid;gap:20px;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
}
.card {
    background:var(--muted);border:1px solid var(--stroke);
    border-radius:16px;box-shadow:var(--shadow);overflow:hidden;
    transform:translateY(30px);opacity:0;transition:all .4s ease;
}
.card.show {transform:translateY(0);opacity:1}
.card img {width:100%;height:200px;object-fit:cover}
.card h3 {margin:15px;color:var(--brand-2)}
.card p {margin:0 15px 10px;color:var(--sub)}
.card button {
    margin:15px auto;display:block;
    background:linear-gradient(135deg,var(--brand),var(--brand-2));
    color:#0b0d12;border:none;padding:10px 20px;
    border-radius:12px;font-weight:600;cursor:pointer;
    transition: all .3s ease-in-out;
    box-shadow: 0 0 15px var(--brand-2), inset 0 0 10px rgba(255,255,255,0.2);
}

/* BOTÃO PIX ADICIONAL */
.pix-container {
    text-align:center;
    margin:30px 0;
}
.pix-container a.btn.primary {
    font-size:18px;
    padding:12px 30px;
}

/* SOBRE E CONTATO */
.sobre, .contatos {padding:50px 0;text-align:center}
.sobre p {max-width:700px;margin:0 auto;color:var(--sub);background:rgba(44, 41, 41, 0);padding:20px;border-radius:12px;}
.icones-contato {display:flex;justify-content:center;gap:30px;margin-top:20px;}
.icones-contato img {height:40px;width:auto;transition:transform 0.3s ease;cursor:pointer;}
.icones-contato img:hover { transform:scale(1.1); }

footer {border-top:1px solid var(--stroke);text-align:center;padding:20px;color:var(--sub);margin-top:40px;}

/* Pagamento overlay */
#pagamento {
    position:fixed;top:0;left:0;width:100%;height:100%;
    background-color:rgba(0,0,0,0.8);
    display:none;flex-direction:column;justify-content:center;align-items:center;
    font-size:2rem;color:var(--text);z-index:2000;
}
#pagamento-box {text-align:center;}
#qrCode {display:none;margin-top:20px;width:200px;height:200px;border-radius:16px;}
#qrCode.show {display: block;animation: pulse 2s infinite;}
@keyframes pulse {0% { transform: scale(1); opacity: 0.8; }50% { transform: scale(1.05); opacity: 1; }100% { transform: scale(1); opacity: 0.8; }}
#pagamento h2.loading::after {content: '';display: inline-block;margin-left: 5px;animation: dots 1.5s infinite steps(4, end);}
@keyframes dots {0% { content: ''; }33% { content: '.'; }66% { content: '..'; }100% { content: '...'; }}

/* Barra de progresso */
#progressBarContainer {width: 250px;height: 20px;background: rgba(255,255,255,0.2);border-radius: 12px;margin-top: 20px;overflow: hidden;}
#progressBar {height: 100%;width: 0%;background: linear-gradient(135deg,var(--brand),var(--brand-2));border-radius: 12px;transition: width 0.3s ease;}

/* Nota Fiscal Modal */
#notaFiscal {position: fixed;top: 0; left: 0; right: 0; bottom: 0;background: rgba(0,0,0,0.7);display: none;justify-content: center;align-items: center;z-index: 3000;}
.nota-content {background: white;color: black;padding: 20px;border-radius: 12px;max-width: 400px;text-align: center;box-shadow: 0 10px 25px rgba(0,0,0,.5);}
.nota-content h2 { margin-bottom: 15px; }
.nota-content button {margin-top: 15px;padding: 10px 20px;border: none;border-radius: 8px;background: #0045f5;color: white;font-weight: bold;cursor: pointer;}

/* Toast Pix */
.toast {position: fixed;bottom: 20px;right: 20px;background: var(--brand);color: #fff;padding: 12px 18px;border-radius: 12px;box-shadow: var(--shadow);font-size: 14px;animation: fadeInOut 3s forwards;z-index: 4000;}
@keyframes fadeInOut {0% {opacity: 0; transform: translateY(20px);}10% {opacity: 1; transform: translateY(0);}90% {opacity: 1;}100% {opacity: 0; transform: translateY(20px);}}
</style>
</head>
<body>

<!-- LOGIN PAGE -->
<div id="login-page">
    <div id="login-box">
        <h1>Seja bem-vindo(a) à Kesley Cakes</h1>
        <button class="btn primary" onclick="login()">Entrar</button>
    </div>
</div>

<!-- STORE PAGE -->
<div id="store-page" style="display:none">
    <header>
        <div class="container nav">
            <div class="logo">
                <span class="logo-badge"></span>
                <span>Kesley<strong>Cakes</strong></span>
            </div>
            <nav class="nav-links">
                <a href="#home">Início</a>
                <a href="#produtos">Produtos</a>
                <a href="#sobre">Sobre</a>
                <a href="#contato">Contato</a>
            </nav>
        </div>
    </header>

    <section class="banner" id="home">
        <h1>Delícias caseiras para você</h1>
        <p>Feitos com carinho, como na casa da vovó.</p>
    </section>

    <section class="produtos container" id="produtos">
        <h2>Nossos Bolos</h2>
        <div class="card-container">
            <div class="card">
                <img src="https://i.ytimg.com/vi/mhDl19m8tn0/maxresdefault.jpg" alt="Bolo de chocolate" />
                <h3>Bolo de Chocolate</h3>
                <p>Simples e delicioso.</p>
                <p><strong>R$ 20,00</strong></p>
                <button onclick="comprarProduto('Bolo de Chocolate', 20)">Comprar</button>
            </div>
            <div class="card">
                <img src="https://guiadacozinha.com.br/wp-content/uploads/2021/06/Bolo-vulcao-de-cenoura-com-brigadeiro.jpg" alt="Bolo de Cenoura" />
                <h3>Bolo de Cenoura</h3>
                <p>Com cobertura de chocolate.</p>
                <p><strong>R$ 22,00</strong></p>
                <button onclick="comprarProduto('Bolo de Cenoura', 22)">Comprar</button>
            </div>
            <div class="card">
                <img src="https://bombocadosbs.com.br/wp-content/uploads/2020/02/morango.jpg" alt="Bolo de morango" />
                <h3>Bolo de Morango</h3>
                <p>Sabor do interior.</p>
                <p><strong>R$ 18,00</strong></p>
                <button onclick="comprarProduto('Bolo de Morango', 18)">Comprar</button>
            </div>
        </div>

        <!-- BOTÃO PIX DIRETO -->
       
    </section>

    <section class="sobre container" id="sobre">
        <h2>Sobre Nós</h2>
        <p>Somos uma pequena confeitaria que acredita no poder das receitas tradicionais e do carinho em cada detalhe. Nossos bolos são feitos artesanalmente, com ingredientes selecionados, para trazer aquele gostinho de casa da vovó.</p>
    </section>

    <section class="contatos container" id="contato">
        <h2>Contato</h2>
        <div class="icones-contato">
            <a href="https://wa.me/61994557954" target="_blank" title="WhatsApp">
                <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
            </a>
            <a href="https://instagram.com/minhalojadebolos" target="_blank" title="Instagram">
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram">
            </a>
            <a href="#" id="pixBtn" title="Pix — clique para copiar, pressione e segure para ver o QR">
                <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/pix.svg" 
                     alt="Pix" style="height:40px; width:auto; filter:invert(23%) sepia(20%) saturate(600%) hue-rotate(350deg) brightness(95%) contrast(90%);">
            </a>
        </div>
    </section>

    <footer>
        &copy; <span id="year"></span> Kesley Cakes. Todos os direitos reservados.
    </footer>
</div>

<!-- PAGAMENTO -->
<div id="pagamento">
  <div id="pagamento-box">
    <h2 class="loading">Aguardando pagamento</h2>
    <img id="qrCode" src="C:\Users\Sidnney54183556\Pictures\t2.png" alt="QR Code Pix">
    <div id="progressBarContainer">
        <div id="progressBar"></div>
    </div>
    <button onclick="fecharPix()" class="btn primary" style="margin-top:20px;">Fechar</button>
  </div>
</div>

<!-- NOTA FISCAL -->
<div id="notaFiscal">
    <div class="nota-content">
        <h2>Nota Fiscal</h2>
        <p id="notaDetalhes"></p>
        <button onclick="fecharNota()">Fechar</button>
         
            <a href="https://nubank.com.br/cobrar/ygvil/68a4cfff-08f3-43f2-91f1-c55aa71b52ff" 
               target="_blank" 
               class="btn primary">
               Pagar via Pix
            </a>
        
    </div>
</div>

<script>
document.getElementById('year').textContent = new Date().getFullYear();

function login() {
    document.getElementById('login-page').style.display = 'none';
    document.getElementById('store-page').style.display = 'block';
    const cards = document.querySelectorAll('.card');
    cards.forEach((card, i) => {
        setTimeout(() => { card.classList.add('show'); }, i * 200);
    });
}

function comprarProduto(nome, preco) {
    const pagamento = document.getElementById('pagamento');
    const qr = document.getElementById('qrCode');
    const progressBar = document.getElementById('progressBar');

    pagamento.style.display = 'flex';
    qr.classList.add('show');
    progressBar.style.width = '0%';

    let width = 0;
    const interval = setInterval(() => {
        width += 1;
        progressBar.style.width = width + '%';
        if(width >= 100) clearInterval(interval);
    }, 30);

    setTimeout(() => {
        pagamento.style.display = 'none';
        qr.classList.remove('show');
        document.getElementById('notaDetalhes').innerHTML =
            `Produto: ${nome}<br>Preço: R$ ${preco.toFixed(2)}<br><br>Obrigado pela sua compra!
            volte sempre`;
        document.getElementById('notaFiscal').style.display = 'flex';
    }, 3000);
}

function fecharNota() { 
    document.getElementById('notaFiscal').style.display = 'none'; 
}

function fecharPix() {
    document.getElementById('pagamento').style.display = 'none';
}

// PIX
const chavePix = "61994557954";
function mostrarPix() { document.getElementById('pagamento').style.display = 'flex'; }
function copiarPix() {
    navigator.clipboard.writeText(chavePix).then(() => {
        const toast = document.createElement("div");
        toast.className = "toast";
        toast.textContent = "Chave Pix copiada!";
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 3000);
    }).catch(err => {
        console.error("Erro ao copiar Pix: ", err);
        alert("Não foi possível copiar a chave Pix.");
    });
}

// Setup Pix Button
(function setupPixButton(){
    const btn = document.getElementById('pixBtn');
    if (!btn) return;

    let pressTimer = null;
    let longPress = false;
    const threshold = 650;

    const start = (e) => {
        e.preventDefault();
        longPress = false;
        pressTimer = setTimeout(() => { longPress = true; mostrarPix(); }, threshold);
    };
    const end = (e) => {
        e.preventDefault();
        if (pressTimer) clearTimeout(pressTimer);
        if (!longPress) copiarPix();
    };
    const cancel = () => { if (pressTimer) clearTimeout(pressTimer); };

    btn.addEventListener('mousedown', start);
    btn.addEventListener('mouseup', end);
    btn.addEventListener('mouseleave', cancel);
    btn.addEventListener('touchstart', start, {passive:false});
    btn.addEventListener('touchend', end, {passive:false});
    btn.addEventListener('touchcancel', cancel, {passive:false});
})();
</script>
</body>
</html>
