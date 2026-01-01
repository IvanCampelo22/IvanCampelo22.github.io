<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
:root {
    --bg: #0d1117;
    --panel: #161b22;
    --border: #30363d;
    --text: #c9d1d9;
    --muted: #8b949e;
    --link: #58a6ff;
}

* { box-sizing: border-box; }

body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
    background: var(--bg);
    color: var(--text);
}

.hero {
    text-align: center;
    padding: 72px 20px 48px;
    border-bottom: 1px solid var(--border);
}

.hero h1 {
    margin: 0;
    font-size: 36px;
    font-weight: 600;
}

.subtitle {
    margin: 10px 0 14px;
    color: var(--muted);
    font-size: 15px;
}

.links a {
    color: var(--link);
    text-decoration: none;
}

.links a:hover {
    text-decoration: underline;
}

.container {
    max-width: 960px;
    margin: 0 auto;
    padding: 32px 20px 64px;
}

h2 {
    margin: 0 0 24px;
    font-size: 22px;
    font-weight: 600;
    border-bottom: 1px solid var(--border);
    padding-bottom: 8px;
}

.project {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 20px 22px;
    margin-bottom: 20px;
}

.project h3 {
    margin-top: 0;
    margin-bottom: 10px;
    font-size: 18px;
}

.project p {
    line-height: 1.55;
    color: var(--text);
}

.project strong {
    color: #f0f6fc;
}

.project a {
    color: var(--link);
    text-decoration: none;
}

.project a:hover {
    text-decoration: underline;
}

footer {
    border-top: 1px solid var(--border);
    padding: 20px;
    text-align: center;
    color: var(--muted);
    font-size: 13px;
}
</style>
</head>

<body>

<section class="hero">
    <h1>Ivan Campelo</h1>
    <p class="subtitle">Desenvolvedor Backend Pleno • Python • Django • FastAPI • LangChain • NestJs • Docker • JavaScript • TypeScript • AWS • GCP</p>
    <p class="links">
        <a href="https://github.com/IvanCampelo22" target="_blank">GitHub</a> |
        <a href="https://linkedin.com/in/ivan-campelo-700519202" target="_blank">LinkedIn</a>
    </p>
</section>

<div class="container">

<h2>Projetos</h2>

<div class="project">
<h3>PensionOne</h3>
<p>
Este projeto consiste em um sistema completo para gestão e análise de adesão a planos de previdência privada, desenvolvido para simular e organizar todo o ciclo de relacionamento entre cliente e produto financeiro. A aplicação permite o cadastro detalhado de clientes, a seleção de planos, a realização de aportes adicionais e o gerenciamento de resgates, garantindo controle, rastreabilidade e segurança em cada etapa do processo. O objetivo principal do sistema é oferecer uma visão clara e estruturada da jornada do cliente, apoiando decisões financeiras e proporcionando uma experiência simples e eficiente para usuários e administradores.
</p>
<p><strong>Tecnologias:</strong> FastAPI, Celery, Redis, PostgreSQL, API REST, WebSockets, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/pension-one" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>Askly</h3>
<p>
Askly é uma plataforma backend desenvolvida para empresas que buscam segurança, flexibilidade e escalabilidade no processo de realização de pesquisas de mercado e coleta de NPS (Net Promoter Score). Inspirado na robustez e na experiência dinâmica do Google Forms, o Askly permite a criação de formulários totalmente personalizáveis e sua distribuição por múltiplos canais, incluindo E-mail, WhatsApp e Telegram, aumentando significativamente a taxa de resposta e a qualidade dos dados coletados. A plataforma oferece suporte a lógicas complexas de formulários, processamento automatizado de dados, histórico de respostas e execução de tarefas assíncronas, fornecendo uma infraestrutura completa para análise da experiência do cliente e apoio à tomada de decisão estratégica.
</p>
<p><strong>Tecnologias:</strong> FastAPI, Selenium, SQLAlchemy, PostgreSQL, Docker, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/askly" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>PulseTrends</h3>
<p>
PulseTrends é uma plataforma de automação e coleta de dados desenvolvida para profissionais e empresas que precisam de acesso rápido, confiável e em larga escala às tendências mais relevantes do momento, sem depender da interface manual do Google Trends. O sistema automatiza todo o processo de pesquisa, extração, tratamento e armazenamento de dados de tendências, permitindo consultas personalizadas por tema, região e período, com persistência em banco de dados e preparação dos dados para análises estratégicas e relatórios. A solução foi projetada com foco em alta performance, robustez operacional e escalabilidade, integrando RPA com processamento backend moderno e infraestrutura em nuvem.
</p>
<p><strong>Tecnologias:</strong> FastAPI, SQLAlchemy, PostgreSQL, Docker, GitHub Actions, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/pulse-trends" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>DataForge</h3>
<p>
Este projeto é uma plataforma especializada para empresas que lidam com grandes volumes de transferência de dados entre arquivos Excel e bancos de dados, eliminando processos manuais e reduzindo drasticamente erros operacionais.

A solução permite a execução de consultas e operações diretamente no banco de dados, possibilitando a criação e modelagem de tabelas e esquemas personalizados de acordo com a estrutura de cada arquivo que será importado.
Essa flexibilidade garante que os dados sejam organizados de forma consistente e adaptada a cada necessidade de negócio.

O alto nível de abstração da plataforma possibilita que usuários sem conhecimento técnico aprofundado construam estruturas de dados capazes de alimentar dashboards, relatórios e fluxos de tratamento de informações, promovendo maior autonomia, produtividade e confiabilidade no uso dos dados.
</p>
<p><strong>Tecnologias:</strong> Python, Postgres, Psycopg2, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/data-forge" target="_blank">Ver no GitHub</a></p>
</div>

</div>

<footer>
© <script>document.write(new Date().getFullYear())</script> • Desenvolvido por Ivan Campelo
</footer>

</body>
</html>
