# Auto-Prime-Veiculos
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AutoPrime Veículos</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
    * { margin:0; padding:0; box-sizing:border-box; font-family:'Roboto', sans-serif; }
    body { background:#111; color:#fff; }

    /* BANNER */
    header {
        background: linear-gradient(90deg,#ff0000,#ff9900);
        padding:60px 20px;
        text-align:center;
        position:relative;
    }
    header h1 { font-size:3rem; text-shadow:2px 2px #000; }
    header p { font-size:1.5rem; font-weight:bold; color:#fff; margin-top:10px; }

    /* CONTAGEM REGRESSIVA */
    .countdown { margin-top:20px; font-size:1.4rem; font-weight:bold; color:#fff; text-shadow:1px 1px #000; }

    /* BIO */
    .bio { background:#222; padding:30px 20px; text-align:center; font-size:1.2rem; line-height:1.6; }

    /* CARROS - SLIDER */
    .slider { display:flex; overflow-x:auto; scroll-snap-type:x mandatory; padding:40px 20px; gap:20px; }
    .slider::-webkit-scrollbar { display:none; }
    .car-card { flex:0 0 300px; background:#1a1a1a; border:2px solid #ff0000; border-radius:10px; text-align:center; scroll-snap-align:start; transition:transform 0.3s; }
    .car-card:hover { transform:scale(1.05); }
    .car-card img { width:100%; height:180px; object-fit:cover; }
    .car-card h3 { margin:15px 0 5px; color:#ffcc00; }
    .car-card p { margin-bottom:15px; font-weight:bold; color:#fff; }
    .car-card button { background:#ff0000; border:none; padding:10px 20px; margin-bottom:15px; color:#fff; font-weight:bold; cursor:pointer; border-radius:5px; transition:background 0.3s; }
    .car-card button:hover { background:#cc0000; }

    /* VANTAGENS */
    .advantages { background:#222; padding:40px 20px; text-align:center; }
    .advantages h2 { margin-bottom:20px; color:#ffcc00; }
    .advantages ul { list-style:none; }
    .advantages li { margin:10px 0; font-size:1.2rem; position:relative; }
    .advantages li::before { content:"✔️"; position:absolute; left:-30px; }

    /* DEPOIMENTOS */
    .testimonials { background:#111; padding:40px 20px; text-align:center; }
    .testimonials h2 { color:#ffcc00; margin-bottom:20px; }
    .testimonial { margin-bottom:20px; font-style:italic; }

    /* CONTATO */
    .contact { background:linear-gradient(90deg,#ff0000,#ff9900); padding:40px 20px; text-align:center; }
    .contact h2 { margin-bottom:20px; color:#fff; }
    .contact p { margin:10px 0; font-weight:bold; font-size:1.2rem; }
    .whatsapp-button { display:inline-block; margin-top:15px; background:#25D366; color:#fff; font-weight:bold; padding:15px 25px; border-radius:10px; text-decoration:none; animation:pulse 1.5s infinite; }
    @keyframes pulse { 0%{transform:scale(1);}50%{transform:scale(1.1);}100%{transform:scale(1);} }

    /* FORMULÁRIO */
    form { margin-top:20px; display:flex; flex-direction:column; gap:15px; max-width:400px; margin-left:auto; margin-right:auto; }
    input, textarea { padding:10px; border-radius:5px; border:none; font-size:1rem; }
    button.submit { background:#ff0000; color:#fff; font-weight:bold; padding:12px; border:none; border-radius:5px; cursor:pointer; transition:0.3s; }
    button.submit:hover { background:#cc0000; }

    /* RODAPÉ */
    footer { background:#111; padding:20px; text-align:center; color:#fff; font-size:0.9rem; margin-top:20px; }
</style>
</head>
<body>

<header>
    <h1>AutoPrime Veículos</h1>
    <p>🔥 OFERTAS IMPERDÍVEIS POR TEMPO LIMITADO – GARANTA SEU CARRO HOJE!</p>
    <div class="countdown" id="countdown">Promoção termina em: 00d 00h 00m 00s</div>
</header>

<div class="bio">
Na AutoPrime Veículos você encontra carros novos e seminovos com preços que cabem no seu bolso! Qualidade garantida, financiamento facilitado e atendimento rápido. Mais de 500 clientes satisfeitos! Não perca nossas promoções exclusivas por tempo limitado!
</div>

<section class="slider">
    <div class="car-card">
        <img src="https://www.chevrolet.com.br/content/dam/chevrolet/mercosul/brazil/vehicles/2024/onix/mov/01-images/onix-2024.jpg" alt="Chevrolet Onix 2024">
        <h3>Chevrolet Onix 2024</h3>
        <p>R$ 79.990</p>
        <button>COMPRAR AGORA</button>
    </div>
    <div class="car-card">
        <img src="https://www.hyundai.com.br/on/demandware.static/-/Sites-hyundai-master-catalog/default/dw8f0c60c7/images/2023/hb20.png" alt="HB20 2023">
        <h3>HB20 2023</h3>
        <p>R$ 72.500</p>
        <button>COMPRAR AGORA</button>
    </div>
    <div class="car-card">
        <img src="https://www.toyota.com.br/wp-content/uploads/2022/06/Corolla-2022.jpg" alt="Toyota Corolla 2022">
        <h3>Toyota Corolla 2022</h3>
        <p>R$ 109.900</p>
        <button>COMPRAR AGORA</button>
    </div>
    <div class="car-card">
        <img src="https://www.fiat.com.br/content/dam/fiat-br/vehicles/argo/2023/argo-2023.png" alt="Fiat Argo 2023">
        <h3>Fiat Argo 2023</h3>
        <p>R$ 68.900</p>
        <button>COMPRAR AGORA</button>
    </div>
    <div class="car-card">
        <img src="https://www.jeep.com.br/content/dam/jeep/vehicles/renegade/2021/renegade-2021.png" alt="Jeep Renegade 2021">
        <h3>Jeep Renegade 2021</h3>
        <p>R$ 98.500</p>
        <button>COMPRAR AGORA</button>
    </div>
</section>

<section class="advantages">
    <h2>Por que comprar conosco?</h2>
    <ul>
        <li>Financiamento facilitado em até 60x</li>
        <li>Entrada parcelada</li>
        <li>Avaliamos seu carro na troca</li>
        <li>Garantia de procedência</li>
    </ul>
</section>

<section class="testimonials">
    <h2>Depoimentos de Clientes</h2>
    <p class="testimonial">"Comprei meu carro aqui e foi tudo perfeito! Atendimento top e preço justo." – Maria S.</p>
    <p class="testimonial">"Financiei meu Onix 2024 sem burocracia. Super recomendo!" – João P.</p>
</section>

<section class="contact">
    <h2>Entre em Contato</h2>
    <p>📞 WhatsApp: <a href="https://wa.me/5511953425162" class="whatsapp-button">11953425162</a></p>
    <p>📸 Instagram: <a href="https://www.instagram.com/ferrsyx" target="_blank">@ferrsyx</a></p>
    <p>📍 Endereço: Avenida São Miguel Paulista, São Paulo – SP</p>

    <form>
        <input type="text" placeholder="Seu nome" required>
        <input type="email" placeholder="Seu email" required>
        <textarea placeholder="Mensagem" rows="4" required></textarea>
        <button type="submit" class="submit">Enviar Mensagem</button>
    </form>
</section>

<footer>
AutoPrime Veículos – Realizando sonhos sobre rodas 🚗✨
</footer>

<script>
// CONTAGEM REGRESSIVA
const countdown = document.getElementById('countdown');
// Defina data da promoção (ex: 7 dias a partir de agora)
const promoDate = new Date();
promoDate.setDate(promoDate.getDate() + 7);

function updateCountdown(){
    const now = new Date();
    const diff = promoDate - now;
    if(diff <= 0){
        countdown.innerText = "Promoção encerrada!";
        return;
    }
    const days = Math.floor(diff/(1000*60*60*24));
    const hours = Math.floor((diff/(1000*60*60))%24);
    const minutes = Math.floor((diff/(1000*60))%60);
    const seconds = Math.floor((diff/1000)%60);
    countdown.innerText = `Promoção termina em: ${days}d ${hours}h ${minutes}m ${seconds}s`;
}
setInterval(updateCountdown, 1000);
updateCountdown();
</script>

</body>
</html>
