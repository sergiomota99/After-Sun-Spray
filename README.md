<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Solevita After Sun Spray</title>
  <style>
    /* Estilo base */
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #fdf6ee;
      color: #3e3e3e;
      scroll-behavior: smooth;
    }

    header {
      background-color: #f5e6ce;
      padding: 2rem;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    header h1 {
      margin: 0;
      font-size: 2.5rem;
      animation: fadeIn 2s ease;
    }

    header p {
      font-style: italic;
      color: #6d5f4c;
    }

    #hero-carousel {
  position: relative;
  height: 55vh;
  overflow: hidden;
}

.carousel-slide {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.carousel-slide.active {
  opacity: 1;
  z-index: 1;
}

.hero-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
  text-align: center;
  text-shadow: 0 3px 6px rgba(0,0,0,0.4);
}

.hero-content h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.hero-content p {
  font-size: 1.25rem;
  margin-bottom: 2rem;
}

.cta-button {
  background-color: #f5e6ce;
  color: #3e3e3e;
  padding: 0.8rem 1.5rem;
  border: none;
  border-radius: 8px;
  font-weight: bold;
  text-decoration: none;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
  transition: background 0.3s ease;
}

.cta-button:hover {
  background-color: #e1d1b5;
}


    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }

    .card {
  background: transparent; /* a card não precisa de fundo branco */
  border-radius: 15px;
  box-shadow: none;
  overflow: visible;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: transform 0.3s ease;
  position: relative;
}

.card-image {
  width: 100%;
  height: 220px;
  overflow: hidden;
  border-radius: 15px 15px 0 0;
  box-shadow: 0 4px 10px rgba(0,0,0,0.08);
}

.card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.card-content {
  background: #fff;
  padding: 1rem;
  margin-top: 0px; /* move a caixa branca para baixo da imagem */
  border-radius: 0 0 15px 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.08);
  width: 90%;
  z-index: 2;
  position: relative;
}


    .card:hover {
      transform: translateY(-5px);
    }

    .faq-item {
      margin-bottom: 1.5rem;
    }

    .faq-question {
      cursor: pointer;
      background: #f5e6ce;
      padding: 1rem;
      border-radius: 10px;
      font-weight: bold;
    }

    .faq-answer {
      display: none;
      padding: 0.5rem 1rem;
      background: #fff9f1;
      border-left: 4px solid #e4cfa4;
    }

    footer {
      text-align: center;
      padding: 2rem;
      background-color: #e8dbc5;
      margin-top: 3rem;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(-20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    #lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 9999;
  cursor: zoom-out;
}

#lightbox img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
}

#ideal-para {
  background-color: #fff1dc;
  padding: 4rem 2rem;
  text-align: center;
  border-radius: 20px;
  margin-top: 2rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
}

#ideal-para h2 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #3e3e3e;
}

.ideal-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
}

.ideal-item {
  flex: 1 1 250px;
  max-width: 300px;
  padding: 1rem;
  background: #ffffff;
  border-radius: 15px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  transition: transform 0.3s ease;
}

.ideal-item:hover {
  transform: translateY(-8px);
}

.ideal-item img {
  height: 60px;
  margin-bottom: 1rem;
}

.ideal-item p {
  font-size: 1.1rem;
  color: #4a4035;
  line-height: 1.4;
}

.fade-in {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}

.fade-in:nth-child(2) { transition-delay: 0.5s; }

#cta-compra {
  background-color: #f5e6ce;
  text-align: center;
  padding: 4rem 2rem;
  border-radius: 20px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.05);
  margin: 3rem auto;
  max-width: 800px;
}

#cta-compra h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #3e3e3e;
}

#cta-compra p {
  font-size: 1.2rem;
  color: #5e5241;
  margin-bottom: 2rem;
}

#cta-compra .cta-button {
  font-size: 1rem;
}

.modal {
  display: none;
  position: fixed;
  z-index: 99999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0,0,0,0.6);
  justify-content: center;
  align-items: center;
}

.modal-conteudo {
  background-color: #fff9f1;
  padding: 2rem;
  border-radius: 15px;
  width: 90%;
  max-width: 500px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
  animation: fadeIn 0.5s ease;
  text-align: center;
}

.modal-conteudo h2 {
  margin-top: 0;
}

.modal-conteudo form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1rem;
}

.modal-conteudo input,
.modal-conteudo textarea {
  padding: 0.75rem;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 1rem;
}

.modal-conteudo button {
  background-color: #f5e6ce;
  color: #3e3e3e;
  border: none;
  padding: 0.8rem;
  border-radius: 8px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s ease;
}

.modal-conteudo button:hover {
  background-color: #e1d1b5;
}

.fechar {
  position: absolute;
  top: 1rem;
  right: 1.5rem;
  font-size: 1.5rem;
  cursor: pointer;
  color: #3e3e3e;
}

#formulacao {
  background-color: #fff9f1;
  padding: 3rem 2rem;
  border-radius: 20px;
  margin: 3rem auto;
  max-width: 800px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.05);
  text-align: center;
}

#formulacao h2 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: #6d5f4c;
}

.ingredientes-list {
  list-style: none;
  padding: 0;
  margin: 0;
  font-size: 1.1rem;
  line-height: 1.8;
  color: #3e3e3e;
}

.ingredientes-list li::before {
  content: "🌿 ";
  color: #8cbf26;
}

#scrollToTopBtn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 999;
  background-color: #f5e6ce;
  color: #3e3e3e;
  border: none;
  border-radius: 50%;
  width: 45px;
  height: 45px;
  font-size: 1.5rem;
  font-weight: bold;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  cursor: pointer;
  display: none; /* Escondido inicialmente */
  transition: opacity 0.3s ease, transform 0.3s ease;
}

#scrollToTopBtn:hover {
  background-color: #e1d1b5;
  transform: scale(1.1);
}


  </style>
</head>
<body>

<header>
  <h1>After Sun Spray Caseiro</h1>
  <p>Alívio natural e cuidado profundo para a tua pele após o sol</p>
  <section id="hero-carousel">
    <div class="carousel-slide active" style="background-image: url('inicio1.jpg');">
      <div class="hero-content">
        <h1>After Sun Natural</h1>
        <a href="#intro1" class="cta-button">Descubra os Benefícios</a>
      </div>
    </div>
    <div class="carousel-slide active" style="background-image: url('inicio2.jpg');">
        <div class="hero-content">
          <h1>After Sun Natural</h1>
          <a href="#intro1" class="cta-button">Descubra os Benefícios</a>
        </div>
      </div>
  </section>
</header>


<section id="intro">
  <h2 class="fade-in">Sobre o Produto</h2>
  <p class="fade-in">Após um dia de exposição solar, a pele precisa de cuidados especiais para se regenerar, hidratar e recuperar o seu equilíbrio natural. O AfterSun Spray Caseiro foi desenvolvido com ingredientes 100% naturais, pensado para acalmar a vermelhidão, aliviar a sensação de ardor, prevenir a descamação e promover uma hidratação intensa.</p>
  <p class="fade-in">Este spray refrescante atua de forma suave e eficaz, proporcionando alívio imediato e ajudando a restaurar a saúde da pele. Ideal para todos os tipos de pele, especialmente as mais sensíveis ou irritadas pelo sol.</p>
</section>

<section id="intro1">
    <h2 class="fade-in">Benefícios principais</h2>
    <ul class="benefits-list">
      <li class="fade-in">Acalma a vermelhidão e irritação</li>
      <li class="fade-in">Previne a descamação da pele</li>
      <li class="fade-in">Hidrata profundamente</li>
      <li class="fade-in">Estimula a regeneração natural da pele</li>
      <li class="fade-in">Fórmula 100% natural e caseira, sem químicos agressivos</li>
      <li class="fade-in">Alivia a sensação de ardor</li>
    </ul>
  </on>
  

<on id="benefits" class="fade-in">
  <h2 class="fade-in">Aromas</h2>
  <div class="grid">     
    <div class="card" onclick="openImage('lavanda.jpg')">
      <div class="card-image">
      <img src="lavanda.jpg">
      </div>
      <div class="card-content">
      <h3 align="center">Lavanda</h3>
    </div>
    </div>
    <div class="card" onclick="openImage('limao.jpg')">
      <div class="card-image">
      <img src="limao.jpg">
      </div>
      <div class="card-content">
      <h3 align="center">Limão</h3>
      </div>
    </div>
    <div class="card" onclick="openImage('neutro.jpg')">
        <div class="card-image">
          <img src="neutro.jpg" alt="Natural">
        </div>
        <div class="card-content">
          <h3 align="center">Natural</h3>
        </div>
      </div> 
    <div class="card" onclick="openImage('hotelã.jpg')">
        <div class="card-image">
        <img src="hotelã.jpg">
        </div>
        <div class="card-content">
        <h3 align="center">Hortelã</h3>
      </div>
    </div>
    <div class="card" onclick="openImage('camomila.jpg')">
      <div class="card-image">
      <img src="camomila.jpg">
      </div>
      <div class="card-content">
      <h3 align="center">Camomila</h3>
    </div>
    </div>
  </div>
</on>

<on id="formulacao" class="fade-in">
    <h2>Constituição do Produto</h2>
    <ul class="ingredientes-list">
      <li>Mel ou açúcar mascavado (amarelo)</li>
      <li>Chá verde</li>
      <li>Gel de aloé vera</li>
      <li>Glicerina vegetal</li>
      <li>Óleo vegetal de girassol ou azeite leve</li>
      <li>Óleo de coco fracionado</li>
      <li>Óleo essencial de hortelã, lavanda, camomila e limão</li>
    </ul>
  </on>
  

<on id="ideal-para" class="fade-in">
    <h2>Feito para quem valoriza o essencial</h2>
    <div class="ideal-grid">
      <div class="ideal-item">
        <img src="natural.svg" alt="Natural" />
        <p>Um cuidado pós-solar <strong>natural e eficaz</strong></p>
      </div>
      <div class="ideal-item">
        <img src="ingredientes-seguros.svg" alt="Ingredientes seguros" />
        <p><strong>Ingredientes simples</strong> que respeitam a tua pele</p>
      </div>
      <div class="ideal-item">
        <img src="ecologico.svg" alt="Ecológico" />
        <p>Produzido com <strong>carinho e consciência ecológica</strong></p>
      </div>
    </div>
  </on>

  <on id="cta-compra">
    <h2 class="fade-in">Dá à tua pele o carinho que ela merece</h2>
    <p class="fade-in">Descobre o poder do AfterSun Spray Caseiro — o teu aliado natural nos dias de sol!</p>
    <a href="javascript:void(0)" onclick="abrirModal()" class="cta-button fade-in">Quero experimentar</a>
  </on>

  <div id="modal-contacto" class="modal">
    <div class="modal-conteudo">
      <span class="fechar" onclick="fecharModal()">&times;</span>
      <h2>Fala connosco</h2>
      <p>Envia-nos uma mensagem e entraremos em contacto contigo o mais breve possível.</p>
      <form>
        <input type="text" placeholder="O teu nome" required>
        <input type="email" placeholder="O teu e-mail" required>
        <textarea placeholder="A tua mensagem" rows="4" required></textarea>
        <button type="submit">Enviar</button>
      </form>
    </div>
  </div>
  
  
    

<on id="faq" class="fade-in">
  <h2 class="fade-in">Perguntas Frequentes</h2>
  <div class="faq-item">
    <div class="faq-question">Como usar?</div>
    <div class="faq-answer">Agite bem antes de usar. Aplica diretamente na pele limpa após a exposição solar, deixando absorver naturalmente. Pode ser usado sempre que necessário ao longo do dia.</div>
  </div>
  <div class="faq-item">
    <div class="faq-question">É indicado para todos os tipos de pele?</div>
    <div class="faq-answer">Sim, é ideal para todos os tipos de pele, especialmente as mais sensíveis ou irritadas pelo sol.</div>
  </div>
  <div class="faq-item">
    <div class="faq-question">Pode ser usado por crianças?</div>
    <div class="faq-answer">Sim, mas sempre sob supervisão de um adulto e evitando o contato com olhos.</div>
  </div>
</on>

<button id="scrollToTopBtn" title="Voltar ao topo">↑</button>


<div id="lightbox" onclick="closeImage()">
    <img id="lightbox-img" src="" alt="Imagem ampliada">
</div>
  

<script>
    function abrirModal() {
      document.getElementById('modal-contacto').style.display = 'flex';
    }
  
    function fecharModal() {
      document.getElementById('modal-contacto').style.display = 'none';
    }
  
    // Fecha o modal se clicares fora da área do conteúdo
    window.addEventListener('click', function(event) {
      const modal = document.getElementById('modal-contacto');
      if (event.target === modal) {
        fecharModal();
      }
    });
  </script>

<script>
    const scrollBtn = document.getElementById("scrollToTopBtn");
  
    window.addEventListener("scroll", () => {
      if (window.scrollY > 300) {
        scrollBtn.style.display = "block";
      } else {
        scrollBtn.style.display = "none";
      }
    });
  
    scrollBtn.addEventListener("click", () => {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    });
  </script>
  
<script>
    let currentSlide = 0;
    const slides = document.querySelectorAll('.carousel-slide');
  
    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.remove('active');
        if (i === index) {
          slide.classList.add('active');
        }
      });
    }
  
    function nextSlide() {
      currentSlide = (currentSlide + 1) % slides.length;
      showSlide(currentSlide);
    }
  
    setInterval(nextSlide, 5000); // Muda a cada 5s
  </script>
  
<script>
  // Animação ao rolar
  const ons = document.querySelectorAll("on");
  const observer = new InteronObserver(entries => {
    entries.forEach(entry => {
      if(entry.isInterng){
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1 });

  ons.forEach(sec => observer.observe(sec));

  // FAQ interativo
  document.querySelectorAll('.faq-question').forEach(q => {
    q.addEventListener('click', () => {
      const answer = q.nextElementSibling;
      const isOpen = answer.style.display === 'block';
      document.querySelectorAll('.faq-answer').forEach(a => a.style.display = 'none');
      answer.style.display = isOpen ? 'none' : 'block';
    });
  });
</script>
<script>
    function openImage(src) {
      document.getElementById('lightbox-img').src = src;
      document.getElementById('lightbox').style.display = 'flex';
    }
  
    function closeImage() {
      document.getElementById('lightbox').style.display = 'none';
      document.getElementById('lightbox-img').src = '';
    }
  </script>

<script>
// Aplica fade-in a todos os elementos com a classe .fade-in ao fazer scroll
const fadeEls = document.querySelectorAll('.fade-in');
const observerFade = new InteronObserver(entries => {
  entries.forEach(entry => {
    if (entry.isInterng) {
      entry.target.classList.add('visible');
    }
  });
}, {
  threshold: 0.1
});

fadeEls.forEach(el => observerFade.observe(el));
</script>

</body>
</html>
