<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Ivan Campelo | Backend Developer</title>
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

header {
    padding: 56px 20px 32px;
    text-align: center;
    border-bottom: 1px solid var(--border);
}

header h1 {
    margin: 0;
    font-size: 32px;
    font-weight: 600;
}

header p {
    margin: 8px 0;
    color: var(--muted);
}

header a {
    color: var(--link);
    text-decoration: none;
}

header a:hover {
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

<header>
    <h1>Ivan Campelo</h1>
    <p>Desenvolvedor Backend Pleno • Python • Django • FastAPI • Celery • RabbitMQ</p>
    <p>
        <a href="https://github.com/IvanCampelo22" target="_blank">GitHub</a> |
        <a href="https://linkedin.com/in/ivan-campelo-700519202" target="_blank">LinkedIn</a>
    </p>
</header>

<div class="container">

<h2>Projetos</h2>

<div class="project">
<h3>PensionOne</h3>
<p>
Sistema completo para gestão e análise de adesão a planos de previdência privada. 
Permite cadastro de clientes, seleção de planos, aportes adicionais e resgates, garantindo controle, rastreabilidade e segurança em todo o ciclo do produto.
</p>
<p><strong>Tecnologias:</strong> FastAPI, Celery, Redis, PostgreSQL, API REST, WebSockets, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/pension-one" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>Askly</h3>
<p>
Plataforma backend para pesquisas de mercado e coleta de NPS, com formulários personalizáveis e distribuição via E-mail, WhatsApp e Telegram, processamento automatizado de dados e tarefas assíncronas.
</p>
<p><strong>Tecnologias:</strong> FastAPI, Selenium, SQLAlchemy, PostgreSQL, Docker, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/askly" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>PulseTrends</h3>
<p>
Plataforma de automação e coleta de dados de tendências, com processamento em larga escala, consultas personalizadas e preparação de dados para análises estratégicas.
</p>
<p><strong>Tecnologias:</strong> FastAPI, SQLAlchemy, PostgreSQL, Docker, GitHub Actions, AWS (EC2, RDS)</p>
<p><a href="https://github.com/IvanCampelo22/pulse-trends" target="_blank">Ver no GitHub</a></p>
</div>

<div class="project">
<h3>Bots de Integração Interna</h3>
<p>
Coleção de serviços para integração entre sistemas, incluindo filas, extração de dados e pipelines automáticos.
</p>
<p><strong>Tecnologias:</strong> Python, Celery, RabbitMQ, APIs externas</p>
<p><a href="https://github.com/SEU_USUARIO/REPO" target="_blank">Ver no GitHub</a></p>
</div>

</div>

<footer>
© <script>document.write(new Date().getFullYear())</script> • Desenvolvido por Ivan Campelo
</footer>

</body>
</html>
