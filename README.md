<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Ivan Campelo | Desenvolvedor Backend</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Portfólio de Ivan Campelo, desenvolvedor backend pleno.">
  <style>
    :root {
      --bg: #050816;
      --bg-alt: #0f172a;
      --card: #020617;
      --primary: #38bdf8;
      --primary-soft: rgba(56, 189, 248, 0.1);
      --text: #e5e7eb;
      --muted: #9ca3af;
      --border: #1f2937;
      --radius: 14px;
      --shadow-soft: 0 18px 40px rgba(15, 23, 42, 0.8);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
        "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #0f172a 0, #020617 40%, #000 100%);
      color: var(--text);
      min-height: 100vh;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .page {
      max-width: 1040px;
      margin: 0 auto;
      padding: 2.5rem 1.5rem 3rem;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1.5rem;
      margin-bottom: 2.5rem;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 0.08em;
      font-size: 0.9rem;
      text-transform: uppercase;
      color: var(--muted);
    }

    nav a {
      font-size: 0.9rem;
      margin-left: 1.2rem;
      color: var(--muted);
      position: relative;
    }

    nav a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -4px;
      width: 0;
      height: 2px;
      background: var(--primary);
      transition: width 0.2s ease;
    }

    nav a:hover {
      color: var(--text);
    }

    nav a:hover::after {
      width: 100%;
    }

    /* Hero */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 2fr) minmax(0, 1.3fr);
      gap: 2.5rem;
      align-items: center;
      margin-bottom: 3rem;
    }

    .hero-title {
      font-size: clamp(2.2rem, 4vw, 2.8rem);
      font-weight: 700;
      margin-bottom: 0.75rem;
    }

    .hero-title span {
      color: var(--primary);
    }

    .hero-subtitle {
      font-size: 1rem;
      color: var(--muted);
      max-width: 520px;
      margin-bottom: 1.4rem;
    }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 1.6rem;
    }

    .badge {
      border-radius: 999px;
      padding: 0.25rem 0.8rem;
      font-size: 0.8rem;
      border: 1px solid var(--border);
      background: rgba(15, 23, 42, 0.9);
      color: var(--muted);
    }

    .badge--highlight {
      border-color: var(--primary);
      background: var(--primary-soft);
      color: var(--primary);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
    }

    .btn {
      border-radius: 999px;
      padding: 0.55rem 1.3rem;
      font-size: 0.9rem;
      border: 1px solid transparent;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.4rem;
      transition: transform 0.12s ease, box-shadow 0.12s ease,
        background 0.12s ease, border-color 0.12s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, #0ea5e9, #22c55e);
      color: #0b1120;
      font-weight: 600;
      box-shadow: 0 14px 35px rgba(34, 197, 94, 0.35);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(34, 197, 94, 0.45);
    }

    .btn-ghost {
      background: transparent;
      color: var(--muted);
      border-color: var(--border);
    }

    .btn-ghost:hover {
      border-color: var(--primary);
      color: var(--text);
      transform: translateY(-1px);
    }

    .hero-right {
      background: radial-gradient(circle at top, #1e293b 0, #020617 65%);
      border-radius: 24px;
      padding: 1.7rem 1.7rem 1.4rem;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-tag {
      font-size: 0.75rem;
      color: var(--muted);
      margin-bottom: 0.35rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .hero-name {
      font-size: 1.3rem;
      font-weight: 600;
      margin-bottom: 0.2rem;
    }

    .hero-role {
      font-size: 0.9rem;
      color: var(--primary);
      margin-bottom: 1.2rem;
    }

    .stack-list {
      list-style: none;
      font-size: 0.85rem;
      color: var(--muted);
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.4rem 1rem;
      margin-bottom: 1.5rem;
    }

    .stack-list li::before {
      content: "•";
      color: var(--primary);
      margin-right: 0.4rem;
    }

    .hero-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 0.8rem;
      font-size: 0.8rem;
      color: var(--muted);
      border-top: 1px solid rgba(15, 23, 42, 0.9);
      padding-top: 0.9rem;
    }

    .pill {
      padding: 0.2rem 0.6rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      font-size: 0.75rem;
    }

    /* Sections */
    section {
      margin-bottom: 3rem;
    }

    .section-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 1rem;
    }

    .section-title span {
      color: var(--primary);
    }

    .section-subtitle {
      font-size: 0.9rem;
      color: var(--muted);
      margin-bottom: 1.2rem;
    }

    /* Cards */
    .grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }

    .grid-2 {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .card {
      background: radial-gradient(circle at top left, #0b1120 0, #020617 60%);
      border-radius: var(--radius);
      border: 1px solid var(--border);
      padding: 1.1rem 1.1rem 1rem;
      box-shadow: 0 14px 35px rgba(15, 23, 42, 0.7);
    }

    .card-title {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .card-meta {
      font-size: 0.8rem;
      color: var(--muted);
      margin-bottom: 0.6rem;
    }

    .card-body {
      font-size: 0.85rem;
      color: var(--muted);
      margin-bottom: 0.7rem;
    }

    .tag-list {
      display: flex;
      flex-wrap: wrap;
      gap: 0.35rem;
      margin-top: 0.3rem;
    }

    .tag {
      font-size: 0.7rem;
      padding: 0.15rem 0.55rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      color: var(--muted);
    }

    .tag-primary {
      border-color: var(--primary);
      color: var(--primary);
    }

    /* Experience timeline */
    .timeline {
      border-left: 1px solid var(--border);
      padding-left: 1rem;
      margin-top: 0.5rem;
    }

    .timeline-item {
      margin-bottom: 1.3rem;
      position: relative;
    }

    .timeline-item::before {
      content: "";
      position: absolute;
      left: -9px;
      top: 4px;
      width: 10px;
      height: 10px;
      border-radius: 999px;
      background: var(--primary);
      box-shadow: 0 0 0 4px rgba(56, 189, 248, 0.12);
    }

    .timeline-role {
      font-size: 0.9rem;
      font-weight: 500;
    }

    .timeline-company {
      font-size: 0.85rem;
      color: var(--muted);
    }

    .timeline-period {
      font-size: 0.75rem;
      color: var(--muted);
      margin: 0.15rem 0 0.25rem;
    }

    .timeline-desc {
      font-size: 0.82rem;
      color: var(--muted);
    }

    /* Contact */
    .contact {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 1.2rem;
      align-items: flex-start;
    }

    .contact-item {
      font-size: 0.9rem;
      color: var(--muted);
      margin-bottom: 0.35rem;
    }

    .contact-item span {
      font-weight: 500;
      color: var(--text);
    }

    .social-links {
      display: flex;
      gap: 0.6rem;
      margin-top: 0.6rem;
    }

    .social-links a {
      font-size: 0.8rem;
      padding: 0.3rem 0.7rem;
      border-radius: 999px;
      border: 1px solid var(--border);
      color: var(--muted);
    }

    .social-links a:hover {
      border-color: var(--primary);
      color: var(--text);
    }

    footer {
      border-top: 1px solid rgba(15, 23, 42, 0.9);
      margin-top: 2rem;
      padding-top: 1.2rem;
      font-size: 0.8rem;
      color: var(--muted);
      text-align: center;
    }

    @media (max-width: 860px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }

      nav {
        display: flex;
        flex-wrap: wrap;
      }

      .hero {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-right {
        order: -1;
      }

      .grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .contact {
        grid-template-columns: minmax(0, 1fr);
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div class="logo">IVAN CAMPELO</div>
      <nav>
        <a href="#sobre">Sobre</a>
        <a href="#skills">Stack</a>
        <a href="#projetos">Projetos</a>
        <a href="#experiencia">Experiência</a>
        <a href="#contato">Contato</a>
      </nav>
    </header>

    <main>
      <!-- HERO -->
      <section class="hero" id="topo">
        <div>
          <h1 class="hero-title">
            Olá, eu sou o <span>Ivan Campelo</span>.
          </h1>
          <p class="hero-subtitle">
            Desenvolvedor backend pleno, especializado em construir APIs escaláveis, integrações robustas 
            e automações que conectam dados, serviços e pessoas.
          </p>

          <div class="hero-badges">
            <span class="badge badge--highlight">Backend Pleno · Python</span>
            <span class="badge">Django &amp; FastAPI</span>
            <span class="badge">Arquitetura de serviços</span>
            <span class="badge">Celery · Redis · RabbitMQ</span>
          </div>

          <div class="hero-actions">
            <a href="#projetos" class="btn btn-primary">Ver projetos</a>
            <a href="#contato" class="btn btn-ghost">Entrar em contato</a>
          </div>
        </div>

        <aside class="hero-right">
          <div class="hero-tag">Perfil</div>
          <div class="hero-name">Ivan Campelo</div>
          <div class="hero-role">Desenvolvedor Backend Pleno</div>

          <ul class="stack-list">
            <li>Python · Django · FastAPI</li>
            <li>Celery · Redis · RabbitMQ</li>
            <li>PostgreSQL · MySQL</li>
            <li>Docker · CI/CD</li>
            <li>REST APIs · Integrações</li>
            <li>Boas práticas · SOLID</li>
          </ul>

          <div class="hero-meta">
            <span class="pill">Foco em back-end</span>
            <span>Aberto a novas oportunidades</span>
          </div>
        </aside>
      </section>

      <!-- SOBRE -->
      <section id="sobre">
        <h2 class="section-title"><span>//</span> Sobre</h2>
        <p class="section-subtitle">
          Um pouco sobre quem eu sou e como trabalho.
        </p>
        <div class="card">
          <p class="card-body">
            Sou desenvolvedor backend pleno com experiência em construção de APIs REST,
            automações com filas de mensagens e integrações entre múltiplos sistemas.
            Gosto de trabalhar com problemas reais de negócio, desenhando soluções
            escaláveis, observáveis e bem testadas.
          </p>
          <p class="card-body">
            No dia a dia, trabalho principalmente com <strong>Python</strong>, 
            frameworks como <strong>Django</strong> e <strong>FastAPI</strong>, 
            mensageria com <strong>Celery</strong>, <strong>Redis</strong> e 
            <strong>RabbitMQ</strong>, além de bancos de dados relacionais 
            como <strong>PostgreSQL</strong> e <strong>MySQL</strong>.
          </p>
          <p class="card-body">
            Tenho interesse em arquitetura de software, boas práticas, performance
            e em tornar processos complexos mais simples por meio de automação.
          </p>
        </div>
      </section>

      <!-- SKILLS -->
      <section id="skills">
        <h2 class="section-title"><span>//</span> Stack &amp; Skills</h2>
        <p class="section-subtitle">
          Tecnologias e áreas com as quais tenho mais experiência.
        </p>

        <div class="grid grid-2">
          <div class="card">
            <div class="card-title">Back-end &amp; APIs</div>
            <div class="card-body">
              Desenvolvimento de APIs REST, serviços internos e microsserviços.
            </div>
            <div class="tag-list">
              <span class="tag tag-primary">Python</span>
              <span class="tag">Django</span>
              <span class="tag">FastAPI</span>
              <span class="tag">DRF</span>
              <span class="tag">Autenticação/JWT</span>
            </div>
          </div>

          <div class="card">
            <div class="card-title">Mensageria &amp; Tarefas</div>
            <div class="card-body">
              Processamento assíncrono, filas, workers e automações.
            </div>
            <div class="tag-list">
              <span class="tag">Celery</span>
              <span class="tag">RabbitMQ</span>
              <span class="tag">Redis</span>
              <span class="tag">Crons</span>
            </div>
          </div>

          <div class="card">
            <div class="card-title">Dados &amp; Persistência</div>
            <div class="card-body">
              Modelagem, consultas otimizadas e integrações com bancos de dados.
            </div>
            <div class="tag-list">
              <span class="tag">PostgreSQL</span>
              <span class="tag">MySQL</span>
              <span class="tag">ORMs</span>
              <span class="tag">Migrations</span>
            </div>
          </div>

          <div class="card">
            <div class="card-title">DevOps &amp; Qualidade</div>
            <div class="card-body">
              Entrega contínua, containers e boas práticas de código.
            </div>
            <div class="tag-list">
              <span class="tag">Docker</span>
              <span class="tag">CI/CD</span>
              <span class="tag">Testes</span>
              <span class="tag">Logging</span>
            </div>
          </div>
        </div>
      </section>

      <!-- PROJETOS -->
      <section id="projetos">
        <h2 class="section-title"><span>//</span> Projetos em Destaque</h2>
        <p class="section-subtitle">
          Alguns exemplos de projetos que representam bem o meu perfil de backend.
          (Substitua os links e descrições pelos seus reais.)
        </p>

        <div class="grid">
          <div class="card">
            <div class="card-title">Plataforma de Clipping de Notícias</div>
            <div class="card-meta">Django · Celery · PostgreSQL</div>
            <div class="card-body">
              API para ingestão, classificação e exportação de notícias, com
              processamento assíncrono de arquivos e integração com planilhas.
            </div>
            <div class="tag-list">
              <span class="tag tag-primary">Backend</span>
              <span class="tag">Import/Export</span>
              <span class="tag">Filas</span>
            </div>
            <!-- <a href="https://github.com/seu-usuario/seu-repo" class="card-link">Ver no GitHub</a> -->
          </div>

          <div class="card">
            <div class="card-title">Serviço de Automação de Compras</div>
            <div class="card-meta">FastAPI · RabbitMQ · Integrações</div>
            <div class="card-body">
              Serviço backend para orquestrar cotações e leilões, comunicando com
              sistemas externos via APIs e filas de mensagens.
            </div>
            <div class="tag-list">
              <span class="tag tag-primary">Integrações</span>
              <span class="tag">Workers</span>
              <span class="tag">APIs externas</span>
            </div>
          </div>

          <div class="card">
            <div class="card-title">Módulo de Autenticação &amp; Sessões</div>
            <div class="card-meta">FastAPI · JWT · SQLAlchemy</div>
            <div class="card-body">
              Sistema de autenticação com controle de sessões, expiração de tokens 
              e registro de acessos para múltiplos produtos.
            </div>
            <div class="tag-list">
              <span class="tag tag-primary">Segurança</span>
              <span class="tag">Autenticação</span>
              <span class="tag">JWT</span>
            </div>
          </div>
        </div>
      </section>

      <!-- EXPERIÊNCIA -->
      <section id="experiencia">
        <h2 class="section-title"><span>//</span> Experiência</h2>
        <p class="section-subtitle">
          Um resumo da minha atuação como desenvolvedor backend pleno.
        </p>

        <div class="card">
          <div class="timeline">
            <div class="timeline-item">
              <div class="timeline-role">Desenvolvedor Backend Pleno</div>
              <div class="timeline-company">Empresa / Projeto principal</div>
              <div class="timeline-period">Ano de início – Atual</div>
              <p class="timeline-desc">
                Atuação focada em APIs REST, automações com Celery, integrações com serviços
                externos e melhorias contínuas de performance, qualidade e monitoração.
              </p>
            </div>

            <div class="timeline-item">
              <div class="timeline-role">Desenvolvedor Backend</div>
              <div class="timeline-company">Outros projetos e clientes</div>
              <div class="timeline-period">Experiências anteriores</div>
              <p class="timeline-desc">
                Participação em diferentes projetos envolvendo integrações, mensageria,
                ETL de dados e suporte a times de produto na implementação de novas 
                funcionalidades backend.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- CONTATO -->
      <section id="contato">
        <h2 class="section-title"><span>//</span> Contato</h2>
        <p class="section-subtitle">
          Quer falar sobre projetos, oportunidades ou trocar ideia sobre backend?
        </p>

        <div class="contact">
          <div class="card">
            <p class="contact-item">
              <span>Email:</span> <!-- coloque seu email real -->
              <a href="mailto:seu-email@exemplo.com">seu-email@exemplo.com</a>
            </p>
            <p class="contact-item">
              <span>Localização:</span> Brasil
            </p>
            <p class="contact-item">
              <span>Atuação:</span> Remoto / Híbrido
            </p>

            <div class="social-links">
              <!-- Troque pelos seus links reais -->
              <a href="https://github.com/seu-usuario" target="_blank" rel="noopener noreferrer">GitHub</a>
              <a href="https://www.linkedin.com/in/seu-usuario" target="_blank" rel="noopener noreferrer">LinkedIn</a>
            </div>
          </div>

          <div class="card">
            <div class="card-title">Como posso ajudar</div>
            <div class="card-body">
              • Desenvolvimento de APIs e serviços backend.<br />
              • Integrações entre sistemas, filas e automações.<br />
              • Refino de arquitetura, performance e qualidade de código.<br />
              • Suporte a times de produto na evolução de plataformas.
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      © <span id="year"></span> · Construído por Ivan Campelo.
    </footer>
  </div>

  <script>
    // Atualiza ano automaticamente
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
