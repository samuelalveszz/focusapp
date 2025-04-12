# FocusApp

![Logo](FOCUS.AI_png.png)

Aplicação desenvolvida no âmbito da disciplina de Interação Humano-Computador.

## Funcionalidades

- Adicionar eventos
- Ver calendário
- Definir utilizador
- Ciclos de foco[Uploading mensagens.html…]()<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Messenger</title>
  <link rel="stylesheet" href="estilo_mensagens.css" />
</head>
<body>

  <!-- Topo com título e navegação -->
  <header class="page-header">
    <h1 class="app-title">Messenger</h1>
    <nav class="tabs-nav">
      <button id="mailBtn" class="tab-btn active" onclick="showSection('mail')">Mail</button>
      <button id="socialBtn" class="tab-btn" onclick="showSection('social')">Social</button>
    </nav>
  </header>

  <!-- Conteúdo principal -->
  <main class="content">

    <!-- Seção: Mail -->
    <section id="mail" class="messages-section">
      <div class="message" ondblclick="openMessage('Mensagem de João', 'Precisas de confirmar a reunião amanhã?')">
        <p><strong>Mensagem de João:</strong> Precisas de confirmar a reunião amanhã?</p>
        <div class="suggestions">
          <button onclick="reply('Sim, estarei lá.', this)">Sim, estarei lá.</button>
          <button onclick="reply('Posso confirmar mais tarde?', this)">Posso confirmar mais tarde?</button>
          <button class="keyboard-btn" onclick="location.href='resposta.html';" aria-label="Responder manualmente">
            <svg viewBox="0 0 24 24">
              <path d="M20 5H4c-1.1 0-2 .9-2 2v10c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 12H4V7h16v10zm-9-4H9v-2h2v2zm0-3H9V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zM7 13H5v-2h2v2zm0-3H5V8h2v2zm12 6H5v-2h14v2z"/>
            </svg>
          </button>
        </div>
      </div>

      <div class="message" ondblclick="openMessage('Mensagem de Maria', 'Envie-me por favor os relatórios finais.')">
        <p><strong>Mensagem de Maria:</strong> Envie-me por favor os relatórios finais.</p>
        <div class="suggestions">
          <button onclick="reply('Claro, envio já.', this)">Claro, envio já.</button>
          <button onclick="reply('Vou verificar e já envio.', this)">Vou verificar e já envio.</button>
          <button class="keyboard-btn" onclick="location.href='resposta.html';" aria-label="Responder manualmente">
            <svg viewBox="0 0 24 24">
              <path d="M20 5H4c-1.1 0-2 .9-2 2v10c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 12H4V7h16v10zm-9-4H9v-2h2v2zm0-3H9V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zM7 13H5v-2h2v2zm0-3H5V8h2v2zm12 6H5v-2h14v2z"/>
            </svg>
          </button>
        </div>
      </div>
    </section>

    <!-- Seção: Social -->
    <section id="social" class="messages-section" style="display: none;">
      <div class="message" ondblclick="openMessage('Mensagem de Ana (via Facebook)', 'Vais ao evento de networking?')">
        <p><strong>Mensagem de Ana:</strong> Vais ao evento de networking?</p>
        <div class="network">(via Facebook)</div>
        <div class="suggestions">
          <button onclick="reply('Sim, vejo-te lá!', this)">Sim, vejo-te lá!</button>
          <button onclick="reply('Ainda estou a decidir.', this)">Ainda estou a decidir.</button>
          <button class="keyboard-btn" onclick="location.href='resposta.html';" aria-label="Responder manualmente">
            <svg viewBox="0 0 24 24">
              <path d="M20 5H4c-1.1 0-2 .9-2 2v10c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 12H4V7h16v10zm-9-4H9v-2h2v2zm0-3H9V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zM7 13H5v-2h2v2zm0-3H5V8h2v2zm12 6H5v-2h14v2z"/>
            </svg>
          </button>
        </div>
      </div>

      <div class="message" ondblclick="openMessage('Mensagem de Pedro (via Instagram)', 'Enviaste as fotos do projeto?')">
        <p><strong>Mensagem de Pedro:</strong> Enviaste as fotos do projeto?</p>
        <div class="network">(via Instagram)</div>
        <div class="suggestions">
          <button onclick="reply('Sim, enviei.', this)">Sim, enviei.</button>
          <button onclick="reply('Vou já enviar.', this)">Vou já enviar.</button>
          <button class="keyboard-btn" onclick="location.href='resposta.html';" aria-label="Responder manualmente">
            <svg viewBox="0 0 24 24">
              <path d="M20 5H4c-1.1 0-2 .9-2 2v10c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 12H4V7h16v10zm-9-4H9v-2h2v2zm0-3H9V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zM7 13H5v-2h2v2zm0-3H5V8h2v2zm12 6H5v-2h14v2z"/>
            </svg>
          </button>
        </div>
      </div>
    </section>

    <!-- Botão Voltar no final -->
    <div class="bottom-back">
      <a href="front_page.html" class="back-button" aria-label="Voltar à página anterior">Voltar</a>
    </div>
  </main>

  <script>
    function showSection(section) {
      document.getElementById('mail').style.display = (section === 'mail') ? 'block' : 'none';
      document.getElementById('social').style.display = (section === 'social') ? 'block' : 'none';

      document.getElementById('mailBtn').classList.toggle('active', section === 'mail');
      document.getElementById('socialBtn').classList.toggle('active', section === 'social');
    }

    function reply(message, element) {
      alert(`Resposta enviada: "${message}"`);
      element.closest('.message').classList.add('fade-out');
      setTimeout(() => {
        element.closest('.message').remove();
      }, 500);
    }

    function openMessage(remetente, conteudo) {
      const url = `resposta.html?remetente=${encodeURIComponent(remetente)}&conteudo=${encodeURIComponent(conteudo)}`;
      window.location.href = url;
    }
  </script>
  <script>
    let touchStartX = 0;
    let touchEndX = 0;
  
    const threshold = 50; // Sensibilidade do swipe (em px)
  
    const content = document.querySelector('.content');
  
    content.addEventListener('touchstart', (e) => {
      touchStartX = e.changedTouches[0].screenX;
    });
  
    content.addEventListener('touchend', (e) => {
      touchEndX = e.changedTouches[0].screenX;
      handleGesture();
    });
  
    function handleGesture() {
      const isLeftSwipe = touchStartX - touchEndX > threshold;
      const isRightSwipe = touchEndX - touchStartX > threshold;
  
      if (isLeftSwipe) {
        // Vai para Social
        showSection('social');
      } else if (isRightSwipe) {
        // Vai para Mail
        showSection('mail');
      }
    }
  </script>
  
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>As tuas notícias</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    :root {
      --primary-color: #ffffff;
      --secondary-color: #bdbdbd;
      --background-color: #121212;
      --hover-color: rgba(255, 255, 255, 0.05);
      --border-color: rgba(255, 255, 255, 0.1);
    }

    body {
      margin: 0;
      background-color: var(--background-color);
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      color: var(--primary-color);
      line-height: 1.6;
    }

    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    .header-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 2rem;
      position: sticky;
      top: 0;
      z-index: 100;
      padding: 1rem 0;
      border-bottom: 1px solid var(--border-color);
      background-color: var(--background-color);
    }

    .page-title {
      font-size: 1.6rem;
      font-weight: 600;
      text-align: center;
      flex: 1;
      margin: 0;
    }

    .filter-icon {
      position: absolute;
      right: 0;
      top: 50%;
      transform: translateY(-50%);
      background-color: var(--hover-color);
      border-radius: 8px;
      padding: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      transition: all 0.3s ease;
      cursor: pointer;
      color: var(--primary-color);
    }

    .filter-icon:hover {
      background-color: rgba(255, 255, 255, 0.12);
      transform: translateY(-50%) scale(1.05);
    }

    .news-article {
      border: 1px solid var(--primary-color);
      background-color: transparent;
      padding: 1.5rem;
      border-radius: 12px;
      margin-bottom: 1.5rem;
      transition: all 0.3s ease;
    }

    .news-article:hover {
      background-color: var(--hover-color);
      transform: translateY(-2px);
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
    }

    .news-category {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      margin-bottom: 0.8rem;
      color: var(--secondary-color);
      font-size: 0.9rem;
    }

    .news-category i {
      font-size: 1rem;
    }

    .news-article h3 {
      margin: 0 0 1rem 0;
      font-size: 1.2rem;
      font-weight: 500;
      color: var(--primary-color);
    }

    .news-article p {
      margin: 0;
      color: var(--secondary-color);
      font-size: 0.95rem;
      line-height: 1.6;
    }

    .news-date {
      display: block;
      font-size: 0.8rem;
      color: var(--secondary-color);
      margin-top: 1rem;
    }

    .read-more {
      display: inline-block;
      color: var(--primary-color);
      text-decoration: none;
      font-size: 0.9rem;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      border: 1px solid var(--border-color);
      border-radius: 6px;
      transition: all 0.3s ease;
    }

    .read-more:hover {
      background-color: var(--hover-color);
    }

    .back-button {
      display: inline-block;
      border: 1px solid #ffffff;
      color: var(--primary-color);
      background-color: transparent;
      padding: 12px 24px;
      border-radius: 8px;
      text-decoration: none;
      font-size: 0.95rem;
      transition: all 0.3s ease;
      margin-top: 2rem;
    }

    .back-button:hover {
      background-color: var(--hover-color);
      transform: translateY(-2px);
    }

    @media (max-width: 480px) {
      .container {
        padding: 1rem;
      }

      .page-title {
        font-size: 1.3rem;
      }

      .news-article {
        padding: 1.2rem;
      }

      .news-article h3 {
        font-size: 1.1rem;
      }

      .news-article p {
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="header-bar">
      <h1 class="page-title">As tuas notícias</h1>
      <a href="definicao_utilizador.html#noticias" class="filter-icon" aria-label="Ir para definições">
        <i class="fas fa-sliders-h"></i>
      </a>
    </div>

    <div class="news-article">
      <div class="news-category">
        <i class="fas fa-chart-line"></i>
        Negócios
      </div>
      <h3>Mercado em alta</h3>
      <p>O índice bolsista continua a subir após anúncios otimistas de várias empresas de tecnologia. Analistas preveem um crescimento sustentado para o próximo trimestre.</p>
      <span class="news-date">Publicado em 15 de Março, 2024</span>
    </div>

    <div class="news-article">
      <div class="news-category">
        <i class="fas fa-landmark"></i>
        Política
      </div>
      <h3>Eleições antecipadas</h3>
      <p>Rumores de novas eleições poderão mudar o cenário político nos próximos meses. Especialistas discutem o impacto nas políticas públicas.</p>
      <span class="news-date">Publicado em 14 de Março, 2024</span>
    </div>

    <div class="news-article">
      <div class="news-category">
        <i class="fas fa-futbol"></i>
        Futebol
      </div>
      <h3>Equipa local vence</h3>
      <p>A equipa da cidade conquistou uma vitória importante no campeonato, aproximando-se do título. O treinador destacou o espírito de equipa.</p>
      <span class="news-date">Publicado em 13 de Março, 2024</span>
    </div>

    <a href="front_page.html" class="back-button">Voltar</a>
  </div>
</body>
</html>

<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <!-- Para garantir responsividade em smartphones -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mensagem Detalhada</title>

  <style>
   /* Reset & Tipografia base */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: #121212;
  color: #fafafa;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
  display: flex;
  flex-direction: column;
  height: 100vh;
}

/* Cabeçalho */
.header {
  padding: 16px;
  font-size: 1.2em;
  font-weight: 600;
  border-bottom: 1px solid #2a2a2a;
  background-color: #1a1a1a;
}

/* Área de conteúdo com scroll */
.content-area {
  flex: 1;
  overflow-y: auto;
  padding: 20px 16px;
}

/* Mensagem original em destaque */
.original-message {
  font-size: 1.3em;
  font-weight: 600;
  margin-bottom: 24px;
  line-height: 1.5em;
  word-wrap: break-word;
  border-left: 3px solid #ffffff;
  padding-left: 12px;
  background-color: rgba(255, 255, 255, 0.03);
  border-radius: 6px;
  padding: 16px;
}

/* Caixa de resposta fixa no fundo */
.reply-box {
  display: flex;
  flex-direction: column;
  padding: 12px 16px;
  background-color: #1e1e1e;
  border-top: 1px solid #2a2a2a;
}

/* Caixa de texto para resposta */
.reply-box textarea {
  resize: none;
  padding: 14px;
  border: 1px solid #ffffff;
  background-color: transparent;
  color: #ffffff;
  font-size: 1em;
  border-radius: 8px;
  margin-bottom: 10px;
  transition: border 0.3s ease, background-color 0.3s ease;
}

.reply-box textarea:focus {
  border-color: #ffffff;
  background-color: rgba(255, 255, 255, 0.05);
  outline: none;
}

/* Botão de enviar */
.reply-box button {
  border: 1px solid #ffffff;
  background-color: transparent;
  color: #ffffff;
  padding: 12px;
  font-size: 1em;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.reply-box button:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-1px);
}

/* Responsivo */
@media (max-width: 600px) {
  .header {
    font-size: 1.1em;
  }

  .original-message {
    font-size: 1.15em;
  }

  .reply-box textarea,
  .reply-box button {
    font-size: 0.95em;
  }
}

  </style>
</head>
<body>
  <!-- Cabeçalho: Remetente -->
  <div class="header" id="remetente"></div>

  <!-- Área principal com a mensagem original -->
  <div class="content-area">
    <div class="original-message" id="conteudo"></div>
  </div>

  <!-- Caixa de resposta fixa no rodapé -->
  <div class="reply-box">
    <textarea id="resposta" rows="3" placeholder="Escreve a tua resposta..."></textarea>
    <button onclick="enviarResposta()">Enviar Resposta</button>
  </div>

  <script>
    // Função para obter parâmetros da URL (remetente e conteudo)
    function getQueryParam(param) {
      const urlParams = new URLSearchParams(window.location.search);
      return urlParams.get(param);
    }

    // Preenche a página com dados da querystring
    document.getElementById('remetente').textContent = getQueryParam('remetente') || 'Remetente';
    document.getElementById('conteudo').textContent  = getQueryParam('conteudo')  || 'Conteúdo da mensagem';

    // Função simples para enviar resposta (exemplo)
    function enviarResposta() {
  const resposta = document.getElementById('resposta').value.trim();
  if (!resposta) {
    alert('Por favor, escreve uma resposta antes de enviar.');
    return;
  }
  alert(`Resposta enviada: "${resposta}"`);
  document.getElementById('resposta').value = '';

  // Volta automaticamente para a página anterior após 500ms (para dar tempo de ler o alert)
  setTimeout(() => {
    window.history.back();
  }, 500);
}

  </script>
</body>
</html>


<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="FOCUS - Aplicação de produtividade com IA" />
  <meta name="theme-color" content="#121212" />
  <title>FOCUS</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      display: flex;
      height: 100vh;
      align-items: center;
      justify-content: center;
      background-color: #121212;
      color: #ffffff;
      position: relative;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    @media (prefers-color-scheme: light) {
      body {
        background-color: #ffffff;
        color: #121212;
      }
      .option-card {
        border-color: #121212;
      }
      .option-desc {
        color: #666;
      }
      .settings-gear {
        background-color: #f5f5f5;
        color: #666;
      }
      .settings-gear:hover {
        color: #121212;
      }
      .option-icon {
        background-color: #f5f5f5;
      }
      .focus-cycle .option-icon {
        background-color: #e3f2fd;
      }
      .neutral-phone .option-icon {
        background-color: #f3e5f5;
      }
    }

    .settings-gear {
      position: fixed;
      top: 20px;
      right: 20px;
      width: 40px;
      height: 40px;
      background-color: #1e1e1e;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: transform 0.3s ease;
      color: #bdbdbd;
      font-size: 20px;
      z-index: 1000;
    }

    .settings-gear:hover {
      transform: rotate(90deg);
      color: #ffffff;
    }

    .container {
      text-align: center;
      max-width: 375px;
      width: 90%;
      padding: 20px;
      margin: 0 auto;
      position: relative;
    }

    @media (max-width: 480px) {
      .container {
        width: 95%;
        padding: 15px;
      }
      
      .logo {
        width: 160px;
      }
      
      h1 {
        font-size: 1.75rem;
      }
      
      .option-card {
        padding: 15px;
      }
    }

    .logo {
      width: 200px;
      height: auto;
      display: block;
      margin: 0 auto 0.8rem auto;
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 0.5rem;
      margin-top: 0;
      text-align: center;
    }

    p.subtitle {
      margin-bottom: 2rem;
      font-size: 1rem;
      color: #ccc;
    }

    .option-card {
      border: 1px solid #ffffff;
      background-color: transparent;
      padding: 18px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      gap: 15px;
      cursor: pointer;
      margin-bottom: 16px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .option-card:hover, .option-card:active {
      transform: translateY(-2px);
    }

    .focus-cycle {
      border-color: #2196f3;
    }

    .focus-cycle:hover {
      background-color: rgba(33, 150, 243, 0.1);
    }

    .neutral-phone {
      border-color: #9c27b0;
    }

    .neutral-phone:hover {
      background-color: rgba(156, 39, 176, 0.1);
    }

    .option-icon {
      width: 48px;
      height: 48px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
      color: #ffffff;
      flex-shrink: 0;
    }

    .focus-cycle .option-icon {
      background-color: rgba(33, 150, 243, 0.2);
    }

    .neutral-phone .option-icon {
      background-color: rgba(156, 39, 176, 0.2);
    }

    .option-content {
      flex: 1;
      text-align: left;
    }

    .option-title {
      font-size: 1.1rem;
      font-weight: 500;
      color: #ffffff;
      margin-bottom: 4px;
    }

    .option-desc {
      font-size: 0.9rem;
      color: #bdbdbd;
    }

    .cancel-btn {
      border: 1px solid #666;
      background-color: transparent;
      padding: 8px 16px;
      border-radius: 8px;
      font-size: 0.9rem;
      color: #666;
      cursor: pointer;
      transition: all 0.3s ease;
      margin-top: 1.5rem;
      display: inline-block;
      text-align: center;
    }

    .cancel-btn:hover, .cancel-btn:active {
      background-color: rgba(255, 255, 255, 0.1);
      color: #ffffff;
      border-color: #ffffff;
    }

    .cancel-btn:focus {
      outline: 2px solid #ffffff;
      outline-offset: 2px;
    }
  </style>
</head>
<body>
  <div class="settings-gear" onclick="location.href='definicao_utilizador.html';" role="button" aria-label="Configurações" tabindex="0">
    &#9881;
  </div>

  <div class="container">
    <img src="FOCUS.AI_png.png" alt="Focus Logo" class="logo" />
    <h1>Ser Produtivo com IA.</h1>
    <p class="subtitle">Como é que deseja começar?</p>

    <div class="option-card focus-cycle" onclick="location.href='focusCycle.html';" role="button" aria-label="Iniciar Focus Cycle" tabindex="0">
      <div class="option-icon">
        <i class="fas fa-clock"></i>
      </div>
      <div class="option-content">
        <div class="option-title">Focus Cycle</div>
        <div class="option-desc">Cycle between focus and break periods</div>
      </div>
    </div>

    <div class="option-card neutral-phone" onclick="location.href='front_page.html';" role="button" aria-label="Usar telefone normalmente" tabindex="0">
      <div class="option-icon">
        <i class="fas fa-mobile-alt"></i>
      </div>
      <div class="option-content">
        <div class="option-title">Neutral Phone</div>
        <div class="option-desc">Use your phone normally</div>
      </div>
    </div>

    <button class="cancel-btn" onclick="handleCancel()" aria-label="Cancelar e sair da aplicação">Cancel</button>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', function() {
      const clickableElements = document.querySelectorAll('[role="button"]');
      
      clickableElements.forEach(element => {
        element.addEventListener('keypress', function(e) {
          if (e.key === 'Enter' || e.key === ' ') {
            e.preventDefault();
            this.click();
          }
        });
      });

      function handleCancel() {
        const confirmed = confirm('Deseja realmente sair da app Focus?');
        if (confirmed) {
          document.body.style.opacity = '0';
          setTimeout(() => {
            window.close();
          }, 300);
        }
      }

      document.body.style.opacity = '0';
      setTimeout(() => {
        document.body.style.transition = 'opacity 0.3s ease';
        document.body.style.opacity = '1';
      }, 100);
    });
  </script>
</body>[Uploading front_page.html…]()<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <!-- Para comportamento responsivo em telemóveis -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FOCUS</title>
  <style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
}

body {
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
  background-color: #121212;
  color: #ffffff;
  position: relative;
}

.container {
  text-align: center;
  max-width: 375px;
  width: 100%;
  padding: 20px;
  margin: 0 auto;
  position: relative;
}

.logo,
.focus-logo {
  width: 140px;              /* Tamanho consistente e visível */
  max-width: 60%;            /* Para adaptar a ecrãs mais pequenos */
  height: auto;
  display: block;            /* Centraliza naturalmente com margin auto */
  margin: 0 auto 0.8rem auto; /* Espaço inferior reduzido para aproximação ao título */
  cursor: pointer;
  transition: transform 0.3s ease;
}

.logo:hover,
.focus-logo:hover {
  transform: scale(1.03);    /* Feedback visual subtil ao hover */
}


.notifications {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 1.5rem;
}

.notification {
  border: 1px solid #ffffff;
  background-color: transparent;
  padding: 18px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.notification:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.notification h4 {
  margin-bottom: 5px;
  font-size: 1.1rem;
  font-weight: 500;
}

.notification p {
  font-size: 0.9rem;
  color: #bdbdbd;
}

.settings-gear {
  position: fixed;
  top: 20px;
  right: 20px;
  width: 40px;
  height: 40px;
  background-color: #1e1e1e;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
  color: #bdbdbd;
  font-size: 20px;
  z-index: 1000;
}

.settings-gear:hover {
  background-color: #292929;
  color: #ffffff;
  transform: rotate(90deg);
}
.back-home-btn {
  position: fixed;
  top: 20px;
  left: 20px;
  display: flex;
  align-items: center;
  gap: 6px;
  padding: 8px 12px;
  background-color: transparent;
  border: 1px solid #ffffff;
  border-radius: 6px;
  color: #ffffff;
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 500;
  transition: background-color 0.3s ease, transform 0.2s ease;
  z-index: 1000;
}

.back-home-btn:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-1px);
}

.back-home-btn .icon {
  width: 18px;
  height: 18px;
  fill: #ffffff;
  transition: fill 0.3s ease;
}

.neutral-title {
  text-align: center;
  font-size: 1.6rem;
  font-weight: 600;
  color: #bdbdbd;
  margin: 0 0 1rem 0; /* reduzido para aproximar dos botões */
}

.container .option-card {
  margin-bottom: 1rem; /* menos espaço entre botões */
}

  </style>
</head>
<body>
  <a href="selecao.html" class="back-home-btn" aria-label="Voltar à página principal">
    <svg viewBox="0 0 24 24" class="icon">
      <path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/>
    </svg>
    Home
  </a>
  
  <div class="container">
    <!-- Substitui aqui o texto "FOCUS" pelo teu LOGO PNG -->
    <!-- Ajusta o 'src' para o caminho correto do teu ficheiro PNG -->
    <img 
      class="focus-logo" 
      src="FOCUS.AI_png.png" 
      alt="Focus Logo"
      onclick="location.href='focusCycle.html';" 
    />
    <h1 class="neutral-title">Neutral Phone</h1>

    <div class="container">
      <!-- Ícone de definições -->
      <div class="settings-gear" onclick="location.href='definicao_utilizador.html';">
          ⚙️
      </div>
    <div class="notifications">
      <div class="notification" onclick="location.href='mensagens.html';">
        <h4>Gestão de Mensagens</h4>
        <p>Organiza as tuas mensagens diárias de forma eficaz.</p>
      </div>
      <div class="notification" onclick="location.href='calendario.html';">
        <h4>Calendário</h4>
        <p>Consulta e gere os teus compromissos facilmente.</p>
      </div>
       <!-- Nova secção para “As tuas notícias” -->
       <div class="notification" onclick="location.href='noticias.html';">
        <h4>As tuas notícias</h4>
        <p>Mantém-te informado sobre o que realmente importa.</p>
      </div>
    </div>
  </div>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fundo iPhone</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            height: 100%;
            overflow: hidden;
        }

        .fullscreen-image {
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <!-- A imagem ocupa todo o ecrã e é clicável -->
    <a href="selecao.html">
        <img 
            src="imagem fundo iphone.png" 
            class="fullscreen-image" 
            alt="Interface iPhone"
            onclick="window.location.href='selecao.html';"
        >
    </a>
</body>
</html>
<!DOCTYPE html> 
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FOCUS CYCLE</title>
  <style>
    body {
      background-color: #121212;
      color: #ffffff;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      overflow: hidden;
      position: relative;
    }

    body::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(45deg, #1a1a1a, #2a2a2a, #121212, #1a1a1a);
      background-size: 400% 400%;
      z-index: -1;
      animation: gradientShift 20s ease infinite;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .cycle-container {
      text-align: center;
      margin-bottom: 40px;
      position: relative;
    }

    .cycle-logo {
      width: 130%;
      max-width: 140px;
      height: auto;
      margin-bottom: 20px;
    }

    .title {
      color: #e0e0e0;
      font-size: 1.2rem;
      margin-bottom: 30px;
      font-weight: 300;
      letter-spacing: 1px;
    }

    .timer-container {
      position: relative;
      width: 200px;
      height: 200px;
      margin: 0 auto;
    }

    .timer-circle {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: #1a1a1a;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 2px solid rgba(255, 255, 255, 0.1);
    }

    .timer-progress {
      position: absolute;
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: conic-gradient(#e0e0e0 0%, transparent 0%);
      transition: background 1s linear;
    }

    .bottom-buttons {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 15px;
      margin-top: 20px;
    }

    .action-btn {
      background-color: rgba(224, 224, 224, 0.1);
      color: #e0e0e0;
      padding: 10px 20px;
      border: 1px solid #e0e0e0;
      border-radius: 20px;
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.3s ease;
      min-width: 150px;
      text-align: center;
    }

    .action-btn:hover {
      background-color: rgba(224, 224, 224, 0.2);
      transform: translateY(-2px);
    }

    .action-btn:active {
      transform: translateY(0);
    }

    .status-text {
      color: #e0e0e0;
      font-size: 0.8rem;
      margin-top: 10px;
      opacity: 0.8;
      letter-spacing: 0.5px;
    }
  </style>
</head>
<body>
  <div class="cycle-container">
    <img 
      class="cycle-logo" 
      src="FOCUS.AI_png.png" 
      alt="Focus Logo"
    />
    <div class="title">MOMENTO DE CONCENTRAÇÃO</div>

    <div class="timer-container">
      <div class="timer-circle">
        <div class="timer-progress" id="timer-progress"></div>
      </div>
    </div>
  </div>

  <div class="bottom-buttons">
    <button class="action-btn" onclick="location.href='break.html'">5-Minute Break</button>
    <button class="action-btn" onclick="location.href='selecao.html'">Finalizar Sessão</button>
  </div>

  <script>
    let totalSeconds = 25 * 60;
    const totalTime = totalSeconds;
    const timerProgress = document.getElementById('timer-progress');

    function updateTimer() {
      const progress = ((totalTime - totalSeconds) / totalTime) * 100;

      // Update progress circle
      timerProgress.style.background = `conic-gradient(#e0e0e0 ${progress}%, transparent ${progress}%)`;

      if (totalSeconds <= 0) {
        timerProgress.style.background = `conic-gradient(#e0e0e0 100%, transparent 100%)`;
      } else {
        totalSeconds--;
        setTimeout(updateTimer, 1000);
      }
    }

    // Initialize timer
    updateTimer();
  </script>
</body>
</html>



</html>

[Uploading adicionar_evento.html…]()<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Adicionar Evento</title>
  <style>
    :root {
      --primary-bg: #121212;
      --secondary-bg: rgba(255, 255, 255, 0.05);
      --hover-bg: rgba(255, 255, 255, 0.1);
      --text-color: #ffffff;
      --border-color: #ffffff;
      --accent-color: #ffffff;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      background-color: var(--primary-bg);
      color: var(--text-color);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      min-height: 100vh;
    }

    .container {
      width: 100%;
      max-width: 400px;
      padding: 24px 16px;
    }

    .title {
      text-align: center;
      font-size: 1.6rem;
      font-weight: 600;
      margin-bottom: 1.5rem;
      color: var(--text-color);
    }

    form {
      background-color: transparent;
      border: 1px solid var(--border-color);
      border-radius: 10px;
      padding: 20px;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      font-weight: 500;
      color: var(--text-color);
      font-size: 0.95rem;
    }

    input[type="text"], input[type="date"], input[type="time"] {
      width: 100%;
      padding: 12px;
      background-color: var(--secondary-bg);
      border: 1px solid var(--border-color);
      border-radius: 6px;
      color: var(--text-color);
      margin-bottom: 16px;
      font-size: 0.95rem;
      transition: all 0.3s ease;
    }

    input[type="text"]:focus, input[type="date"]:focus, input[type="time"]:focus {
      outline: none;
      background-color: var(--hover-bg);
    }

    .save-btn {
      width: 100%;
      background-color: var(--accent-color);
      color: var(--primary-bg);
      border: none;
      padding: 12px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: 500;
      font-size: 0.95rem;
      transition: all 0.3s ease;
    }

    .save-btn:hover {
      background-color: #e0e0e0;
      transform: translateY(-2px);
    }

    .cancel-btn {
      display: block;
      margin-top: 20px;
      padding: 10px 16px;
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--text-color);
      text-decoration: none;
      border: 1px solid var(--border-color);
      border-radius: 6px;
      background-color: transparent;
      transition: all 0.3s ease;
      text-align: center;
    }

    .cancel-btn:hover {
      background-color: var(--hover-bg);
      transform: translateY(-2px);
    }

    @media (max-width: 480px) {
      .container {
        padding: 16px 12px;
      }
      
      form {
        padding: 16px;
      }
      
      input[type="text"], input[type="date"], input[type="time"] {
        padding: 10px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="title">Adicionar Evento</div>

    <form id="eventoForm">
      <label for="titulo">Título do Evento</label>
      <input type="text" id="titulo" name="titulo" placeholder="Ex: Reunião com equipa" required>

      <label for="data">Data</label>
      <input type="date" id="data" name="data" required>

      <label for="hora">Hora</label>
      <input type="time" id="hora" name="hora" required>

      <button type="submit" class="save-btn">Guardar Evento</button>
      <a href="calendario.html" class="cancel-btn">Cancelar</a>
    </form>
  </div>

  <script>
    document.getElementById("eventoForm").addEventListener("submit", function(e) {
      e.preventDefault();
      
      // Aqui podias guardar os dados se necessário...
  
      // Redirecionar após "guardar"
      window.location.href = "calendario.html";
    });
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pausa do Focus Cycle</title>
  <style>
    /* Reset & Base */
    :root {
      --primary-color: #ffffff;
      --secondary-color: #bdbdbd;
      --background-color: #121212;
      --hover-color: rgba(255, 255, 255, 0.05);
      --border-color: rgba(255, 255, 255, 0.1);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      background-color: var(--background-color);
      color: var(--primary-color);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      align-items: center;
      padding: 20px;
      line-height: 1.6;
    }

    /* Topo / Título */
    .break-header {
      text-align: center;
      margin-bottom: 2rem;
      opacity: 0;
      transform: translateY(-20px);
      animation: fadeInDown 0.5s ease forwards;
    }

    .break-header h1 {
      font-size: 1.8rem;
      font-weight: 600;
      margin-bottom: 0.5rem;
    }

    .break-header p {
      color: var(--secondary-color);
      font-size: 0.95rem;
    }

    /* Container de notificações */
    .notifications {
      width: 100%;
      max-width: 600px;
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    /* Card genérico de notificação */
    .notification-card {
      background-color: transparent;
      border: 1px solid var(--primary-color);
      border-radius: 12px;
      padding: 1.5rem;
      transition: all 0.3s ease;
      opacity: 0;
      transform: translateY(20px);
    }

    .notification-card:nth-child(1) {
      animation: fadeInUp 0.5s ease 0.3s forwards;
    }

    .notification-card:nth-child(2) {
      animation: fadeInUp 0.5s ease 0.6s forwards;
    }

    .notification-card:nth-child(3) {
      animation: fadeInUp 0.5s ease 0.9s forwards;
    }

    .notification-card:hover {
      background-color: var(--hover-color);
      transform: translateY(-2px);
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
    }

    .notification-title {
      font-size: 1rem;
      font-weight: 500;
      margin-bottom: 0.5rem;
    }

    .notification-info {
      font-size: 0.9rem;
      color: var(--secondary-color);
      line-height: 1.4;
    }

    /* Resposta rápida */
    .suggestions {
      display: flex;
      gap: 8px;
      margin-top: 1rem;
      align-items: center;
    }

    .suggestions button {
      background-color: transparent;
      color: var(--primary-color);
      border: 1px solid var(--border-color);
      padding: 8px 16px;
      border-radius: 8px;
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.3s ease;
      min-width: 90px;
      text-align: center;
    }

    .suggestions button:hover {
      background-color: var(--hover-color);
      transform: translateY(-2px);
    }

    /* Botão de teclado */
    .keyboard-btn {
      background-color: var(--hover-color);
      border: none;
      padding: 10px;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.3s ease;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .keyboard-btn:hover {
      transform: scale(1.05);
      background-color: rgba(255, 255, 255, 0.12);
    }

    .keyboard-btn svg {
      width: 18px;
      height: 18px;
      fill: var(--primary-color);
    }

    /* Botões inferiores */
    .bottom-buttons {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 2rem;
      width: 80%;
      gap: 1rem;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 0.5s ease 1.2s forwards;
    }

    .cycle-btn, .close-btn {
      text-decoration: none;
      color: var(--primary-color);
      border: 1px solid var(--primary-color);
      border-radius: 8px;
      padding: 8px 16px;
      font-size: 0.85rem;
      transition: all 0.3s ease;
      display: inline-block;
      background-color: transparent;
      cursor: pointer;
      width: 140px;
      text-align: center;
    }

    .cycle-btn:hover, .close-btn:hover {
      background-color: var(--hover-color);
      transform: translateY(-2px);
    }

    /* Animações */
    @keyframes fadeInDown {
      from {
        opacity: 0;
        transform: translateY(-20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Responsivo */
    @media (max-width: 480px) {
      .break-header h1 {
        font-size: 1.6rem;
      }

      .notifications {
        gap: 1.2rem;
      }

      .notification-card {
        padding: 1.2rem;
      }

      .suggestions button {
        font-size: 0.85rem;
        min-width: 80px;
        padding: 6px 12px;
      }

      .keyboard-btn {
        padding: 8px;
      }

      .keyboard-btn svg {
        width: 16px;
        height: 16px;
      }

      .cycle-btn, .close-btn {
        width: 100%;
        max-width: 140px;
        padding: 6px 12px;
        font-size: 0.8rem;
      }
    }
  </style>
</head>
<body>
  <!-- Topo -->
  <div class="break-header">
    <h1>5-Minute Break</h1>
    <p>Durante a tua pausa, mostramos só o que realmente importa.</p>
  </div>

  <!-- Lista de notificações importantes -->
  <div class="notifications">
    <!-- 1) Mensagem importante -->
    <div class="notification-card focus-message">
      <div class="notification-title">Mensagem de Carlos</div>
      <div class="notification-info">
        "Precisas de aprovar o documento urgente antes das 15h"
      </div>
      <div class="suggestions">
        <button onclick="replyQuick('Vou ver já.', this)">Vou ver já.</button>
        <button onclick="replyQuick('Posso tratar disso depois da pausa.', this)">Mais tarde</button>
        <button class="keyboard-btn" onclick="location.href='resposta_focus.html';" aria-label="Responder manualmente">
          <svg viewBox="0 0 24 24">
            <path d="M20 5H4c-1.1 0-2 .9-2 2v10c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 12H4V7h16v10zm-9-4H9v-2h2v2zm0-3H9V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zm3 3h-2v-2h2v2zm0-3h-2V8h2v2zM7 13H5v-2h2v2zm0-3H5V8h2v2zm12 6H5v-2h14v2z"/>
          </svg>
        </button>
      </div>
    </div>

    <!-- 2) Notícia importante -->
    <div class="notification-card">
      <div class="notification-title">Notícia em Destaque</div>
      <div class="notification-info">
        Atualização de segurança disponível para o teu dispositivo.  
      </div>
    </div>

    <!-- 3) Lembrete do calendário -->
    <div class="notification-card">
      <div class="notification-title">Lembrete: Calendário</div>
      <div class="notification-info">
        Tens uma reunião às 16:00 sobre o projeto "Focus App".  
        Verifica se tens tudo pronto!
      </div>
    </div>
  </div>

  <!-- Zona dos botões finais -->
  <div class="bottom-buttons">
    <!-- Botão Voltar ao Cycle -->
    <a href="focusCycle.html" class="cycle-btn" aria-label="Voltar ao ciclo">Voltar ao Cycle</a>
  
    <!-- Botão Fechar -->
    <button onclick="window.location.href='selecao.html'" class="close-btn" aria-label="Fechar notificações">Fechar</button>
  </div>

  <script>
    function replyQuick(msg, element) {
      alert('Resposta rápida: ' + msg);
      // Podes animar ou remover a notificação se quiseres
      element.closest('.notification-card').style.opacity = '0.5';
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Resumo Diário</title>
  <style>
    :root {
      --primary-bg: #121212;
      --secondary-bg: rgba(255, 255, 255, 0.05);
      --hover-bg: rgba(255, 255, 255, 0.1);
      --text-color: #ffffff;
      --border-color: #ffffff;
      --accent-color: #ffffff;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      background-color: var(--primary-bg);
      color: var(--text-color);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      min-height: 100vh;
    }

    .container {
      width: 100%;
      max-width: 400px;
      padding: 24px 16px;
    }

    .title {
      text-align: center;
      font-size: 1.6rem;
      font-weight: 600;
      margin-bottom: 1.5rem;
      color: var(--text-color);
    }

    .section {
      background-color: transparent;
      border: 1px solid var(--border-color);
      border-radius: 10px;
      padding: 16px;
      margin-bottom: 20px;
      transition: transform 0.2s ease;
    }

    .section:hover {
      transform: translateY(-2px);
    }

    .section h2 {
      margin-top: 0;
      font-size: 1.2rem;
      margin-bottom: 10px;
      color: var(--text-color);
    }

    .event {
      background-color: var(--secondary-bg);
      border-radius: 6px;
      padding: 12px;
      margin-bottom: 8px;
      font-size: 0.95rem;
      cursor: pointer;
      transition: all 0.3s ease;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .event:hover {
      background-color: var(--hover-bg);
      transform: translateX(4px);
    }

    .event::before {
      content: "•";
      color: var(--accent-color);
    }

    .no-events {
      color: #999;
      font-style: italic;
      text-align: center;
      padding: 16px;
    }

    .back-btn-left {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 16px;
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--text-color);
      text-decoration: none;
      border: 1px solid var(--border-color);
      border-radius: 6px;
      background-color: transparent;
      transition: all 0.3s ease;
    }

    .back-btn-left:hover {
      background-color: var(--hover-bg);
      transform: translateY(-2px);
    }

    .add-button {
      width: 48px;
      height: 48px;
      margin-top: 20px;
      border-radius: 50%;
      background-color: var(--accent-color);
      color: var(--primary-bg);
      font-size: 1.8rem;
      font-weight: bold;
      text-decoration: none;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.4);
      transition: all 0.3s ease;
    }

    .add-button:hover {
      background-color: #e0e0e0;
      transform: scale(1.08) rotate(90deg);
    }

    .button-container {
      display: flex;
      justify-content: space-between;
      padding: 0 16px;
      margin-top: 30px;
      position: sticky;
      bottom: 20px;
    }

    @media (max-width: 480px) {
      .container {
        padding: 16px 12px;
      }
      
      .section {
        padding: 12px;
      }
      
      .event {
        padding: 10px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="title">Resumo do Dia</div>

    <div class="section">
      <h2>Atividades de Hoje</h2>
      <div id="dailyActivities"></div>
    </div>

    <div class="section">
      <h2>Atividades Futuras Relevantes</h2>
      <div id="futureSuggestions"></div>
    </div>

    <div class="button-container">
      <a href="front_page.html" class="back-btn-left" aria-label="Voltar à página anterior">Voltar</a>
      <a href="adicionar_evento.html" class="add-button" aria-label="Adicionar Evento">+</a>
    </div>
  </div>

  <script>
    // Função para formatar a data
    function formatDate(date) {
      return date.toISOString().split('T')[0];
    }

    // Obter a data atual
    const today = new Date();
    const todayKey = formatDate(today);

    // Gerar próximas 3 datas
    const futureKeys = Array.from({length: 3}, (_, i) => {
      const date = new Date(today);
      date.setDate(today.getDate() + i + 1);
      return formatDate(date);
    });

    // Dados de exemplo (em um caso real, isso viria de um backend)
    const eventsMap = {
      [todayKey]: ['Reunião com equipa às 10:00', 'Estudar IHC'],
      [futureKeys[0]]: ['Início de tarefa semanal', 'Preparar relatório'],
      [futureKeys[1]]: ['Enviar relatório final'],
      [futureKeys[2]]: ['Sessão de estudo com grupo'],
    };

    const dailyContainer = document.getElementById('dailyActivities');
    const futureContainer = document.getElementById('futureSuggestions');

    function renderList(container, events) {
      container.innerHTML = ''; // Limpar container antes de renderizar

      if (!events || events.length === 0) {
        container.innerHTML = '<div class="no-events">Sem atividades.</div>';
        return;
      }

      events.forEach(evt => {
        const div = document.createElement('div');
        div.className = 'event';
        div.textContent = evt;
        div.setAttribute('role', 'button');
        div.setAttribute('tabindex', '0');
        div.onclick = () => {
          // Aqui você pode adicionar mais funcionalidades quando clicar em um evento
          alert(evt);
        };
        container.appendChild(div);
      });
    }

    // Renderizar atividades do dia
    renderList(dailyContainer, eventsMap[todayKey]);

    // Preparar e renderizar atividades futuras
    const futureToConsider = [];
    futureKeys.forEach(key => {
      const events = eventsMap[key] || [];
      const date = new Date(key);
      const formattedDate = date.toLocaleDateString('pt-PT', { day: '2-digit', month: '2-digit' });
      events.forEach(e => futureToConsider.push(`${e} (${formattedDate})`));
    });

    renderList(futureContainer, futureToConsider);
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Definições de Utilizador | FOCUS</title>
  <style>
    :root {
      --primary-color: #ffffff;
      --background-color: #121212;
      --hover-color: rgba(255, 255, 255, 0.1);
      --border-color: #ffffff;
      --text-color: #f2f2f2;
      --transition-speed: 0.3s;
    }

    /* Reset e base */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      background-color: var(--background-color);
      color: var(--text-color);
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      line-height: 1.6;
    }

    /* Cabeçalho */
    header {
      margin: 20px 0;
      font-size: 1.5rem;
      font-weight: 600;
      text-align: center;
      padding: 0 12px;
      color: var(--primary-color);
    }

    /* Menu de abas */
    nav.tabs {
      width: 100%;
      overflow-x: auto;
      white-space: nowrap;
      margin: 15px 0;
      padding-bottom: 5px;
      scrollbar-width: none;
      -ms-overflow-style: none;
    }

    nav.tabs::-webkit-scrollbar {
      display: none;
    }

    nav.tabs button {
      display: inline-block;
      background-color: transparent;
      border: 1px solid var(--border-color);
      border-radius: 20px;
      padding: 8px 16px;
      margin: 0 6px;
      color: var(--primary-color);
      cursor: pointer;
      font-size: 0.95rem;
      transition: all var(--transition-speed) ease;
    }

    nav.tabs button:hover,
    nav.tabs button.active {
      background-color: var(--hover-color);
      transform: translateY(-1px);
    }

    /* Conteúdo das abas */
    .tabcontent {
      display: none;
      width: 90%;
      max-width: 600px;
      margin: 20px auto;
      padding: 20px;
      background-color: transparent;
      border: 1px solid var(--border-color);
      border-radius: 10px;
      transition: all var(--transition-speed) ease;
      opacity: 0;
      transform: translateY(10px);
    }

    .tabcontent.active {
      display: block;
      opacity: 1;
      transform: translateY(0);
    }

    /* Inputs & Formulários */
    input[type="text"],
    input[type="email"],
    input[type="password"],
    textarea,
    select {
      width: 100%;
      box-sizing: border-box;
      padding: 12px;
      background-color: transparent;
      border: 1px solid var(--border-color);
      border-radius: 6px;
      color: var(--text-color);
      margin-bottom: 12px;
      font-size: 0.95rem;
      transition: all var(--transition-speed) ease;
    }

    input:focus,
    textarea:focus,
    select:focus {
      outline: none;
      border-color: var(--primary-color);
      background-color: var(--hover-color);
    }

    /* Checkboxes */
    .checkbox-group {
      display: flex;
      align-items: center;
      margin-bottom: 12px;
      font-size: 1rem;
      color: var(--text-color);
      cursor: pointer;
    }

    input[type="checkbox"] {
      appearance: none;
      -webkit-appearance: none;
      width: 18px;
      height: 18px;
      border: 2px solid var(--border-color);
      border-radius: 5px;
      background-color: transparent;
      margin-right: 10px;
      cursor: pointer;
      position: relative;
      transition: all var(--transition-speed) ease;
      vertical-align: middle;
    }

    input[type="checkbox"]:checked {
      background-color: var(--primary-color);
      border-color: var(--primary-color);
    }

    input[type="checkbox"]:checked::after {
      content: '';
      position: absolute;
      left: 5px;
      top: 1px;
      width: 4px;
      height: 9px;
      border: solid var(--background-color);
      border-width: 0 2px 2px 0;
      transform: rotate(45deg);
    }

    /* Botões */
    .form-actions {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      margin-top: 20px;
    }

    .save-btn,
    .back-btn {
      flex: 1;
      text-align: center;
      padding: 10px 16px;
      font-size: 0.95rem;
      font-weight: 500;
      border-radius: 6px;
      border: 1px solid var(--border-color);
      background-color: transparent;
      color: var(--primary-color);
      cursor: pointer;
      transition: all var(--transition-speed) ease;
      text-decoration: none;
    }

    .save-btn:hover,
    .back-btn:hover {
      background-color: var(--hover-color);
      transform: translateY(-1px);
    }

    /* Responsividade */
    @media (max-width: 480px) {
      header {
        font-size: 1.3rem;
      }

      nav.tabs button {
        padding: 6px 12px;
        font-size: 0.9rem;
      }

      .tabcontent {
        padding: 15px;
      }

      .save-btn,
      .back-btn {
        font-size: 0.9rem;
        padding: 8px 16px;
      }
    }

    /* Acessibilidade */
    .sr-only {
      position: absolute;
      width: 1px;
      height: 1px;
      padding: 0;
      margin: -1px;
      overflow: hidden;
      clip: rect(0, 0, 0, 0);
      border: 0;
    }

    /* Animações */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .tabcontent.active {
      animation: fadeIn var(--transition-speed) ease forwards;
    }
  </style>
</head>
<body>
  <header>FOCUS - Definições de Utilizador</header>

  <nav class="tabs" role="tablist">
    <button class="tablink active" data-tab="personalizacao" role="tab" aria-selected="true">Personalização IA</button>
    <button class="tablink" data-tab="contas" role="tab" aria-selected="false">Contas</button>
    <button class="tablink" data-tab="noticias" role="tab" aria-selected="false">Notícias</button>
    <button class="tablink" data-tab="permissoes" role="tab" aria-selected="false">Permissões</button>
    <button class="tablink" data-tab="seguranca" role="tab" aria-selected="false">Segurança</button>
    <button class="tablink" data-tab="notificacoes" role="tab" aria-selected="false">Notificações</button>
  </nav>

  <!-- Conteúdo das abas -->
  <section id="personalizacao" class="tabcontent active" role="tabpanel" aria-labelledby="personalizacao-tab">
    <h3>Personalização IA</h3>
    <input type="text" placeholder="Nome / Apresentação" aria-label="Nome ou apresentação"/>
    <textarea rows="3" placeholder="Bio ou descrição..." aria-label="Bio ou descrição"></textarea>
    <select aria-label="Selecione o tema">
      <option>Tema escuro</option>
      <option>Tema claro</option>
      <option>Automático</option>
    </select>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <section id="contas" class="tabcontent" role="tabpanel" aria-labelledby="contas-tab">
    <h3>Contas</h3>
    <div class="checkbox-group">
      <input type="checkbox" id="instagram">
      <label for="instagram">Instagram</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="facebook">
      <label for="facebook">Facebook</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="whatsapp">
      <label for="whatsapp">WhatsApp</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="gmail">
      <label for="gmail">Gmail</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="calendar">
      <label for="calendar">Google Calendar</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="outlook">
      <label for="outlook">Outlook</label>
    </div>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <section id="noticias" class="tabcontent" role="tabpanel" aria-labelledby="noticias-tab">
    <h3>Notícias</h3>
    <div class="checkbox-group">
      <input type="checkbox" id="tecnologia">
      <label for="tecnologia">Tecnologia</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="negocios">
      <label for="negocios">Negócios</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="desporto">
      <label for="desporto">Desporto</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="entretenimento">
      <label for="entretenimento">Entretenimento</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="ciencia">
      <label for="ciencia">Ciência e Saúde</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="politica">
      <label for="politica">Política</label>
    </div>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <section id="permissoes" class="tabcontent" role="tabpanel" aria-labelledby="permissoes-tab">
    <h3>Permissões</h3>
    <div class="checkbox-group">
      <input type="checkbox" id="dm">
      <label for="dm">Acesso a direct messages</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="calendarios">
      <label for="calendarios">Acesso a calendários privados</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="emails">
      <label for="emails">Leitura de e-mails antigos</label>
    </div>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <section id="seguranca" class="tabcontent" role="tabpanel" aria-labelledby="seguranca-tab">
    <h3>Segurança</h3>
    <input type="email" placeholder="Email de recuperação" aria-label="Email de recuperação"/>
    <input type="password" placeholder="Nova password" aria-label="Nova password"/>
    <div class="checkbox-group">
      <input type="checkbox" id="2fa">
      <label for="2fa">Autenticação dois fatores (2FA)</label>
    </div>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <section id="notificacoes" class="tabcontent" role="tabpanel" aria-labelledby="notificacoes-tab">
    <h3>Notificações</h3>
    <div class="checkbox-group">
      <input type="checkbox" id="mensagens">
      <label for="mensagens">Mensagens importantes</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="alertas">
      <label for="alertas">Alertas de calendário</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="novidades">
      <label for="novidades">Novidades relevantes</label>
    </div>
    <div class="form-actions">
      <button class="save-btn">Guardar</button>
      <a href="selecao.html" class="back-btn">Voltar</a>
    </div>
  </section>

  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const tabs = document.querySelectorAll('.tablink');
      const contents = document.querySelectorAll('.tabcontent');

      // Função para mudar de aba
      const switchTab = (tab) => {
        tabs.forEach(t => {
          t.classList.remove('active');
          t.setAttribute('aria-selected', 'false');
        });
        contents.forEach(c => c.classList.remove('active'));

        tab.classList.add('active');
        tab.setAttribute('aria-selected', 'true');
        document.getElementById(tab.dataset.tab).classList.add('active');
      };

      // Adiciona event listeners para as abas
      tabs.forEach(tab => {
        tab.addEventListener('click', () => switchTab(tab));
        tab.addEventListener('keydown', (e) => {
          if (e.key === 'Enter' || e.key === ' ') {
            e.preventDefault();
            switchTab(tab);
          }
        });
      });

      // Verifica hash da URL
      const hash = window.location.hash.substring(1);
      if (hash) {
        const tabButton = document.querySelector(`.tablink[data-tab="${hash}"]`);
        if (tabButton) switchTab(tabButton);
      }
    });
  </script>
</body>
</html>





