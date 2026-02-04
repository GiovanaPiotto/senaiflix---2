//# Meu primeiro repositorio 
Feito na aula de Git e GitHub//

<!DOCTYPE html>
<html Lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Primeira Página HTML + CSS</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <header class="topo">

        <img src="" alt="Logotipo da Pagina" class="logo" />

        <h1>HTML + CSS: Fundamentos</h1>
        <p class="subtitulo">Estrutura, tags básicas, seletores e box model</p>
        <nav aria-label="Navegação principal">
            <ul class="menu">
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#conteúdo">Conteúdo</a></li>
                <li><a href="#tabela">Tabela</a></li>
                <li><a href="contato">Contato</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section id="sobre" class="card">
            <h2>Sobre esta página</h2>
            <p>Esta é uma página de exemplo para ensinar <strong>HTML</strong> e <em>CSS</em> do zero. Observe a
                estrutura do código, os comentários e o estilo aplicado</p>
            <h3>O que vamos ver:</h3>
            <ul>
                <li>Estrutura básica do HTML</li>
                <li>Seletores CSS: elemento, classe e id</li>
                <li>Box model: margin, padding e border</li>
                <li>Links, imagens, listas e tabelas</li>
                <li>Formulário simples e responsividade</li>
            </ul>
            <p>
                Dica: consulte a documentação do MDN
                <a href="https://developer.mozilla.org/en-US/" target="_blank">aqui
                </a>
            </p>

        </section>

        <section id="conteudo" class="card">
            <h2>Conceitos de CSS essenciais</h2>
            <article class="caixa">
                <h3>Seletores &amp; Especificidade</h3>
                <p>Regras CSS podem mirar em elemento, classes ou ids
                    Quando há conflito, o navegador escolhe pela prioridade:
                    id > class > elemento
                </p>
                <p id="destaque">Este parágrafo tem um ID para destaque</p>
            </article>

            <article class="caixa">
                <h3>Box Model</h3>
                <p>Todo elemento em bloco possui content, padding, border e margin.
                </p>
                <div class="box-model-demo">Sou uma caixa</div>
            </article>
            <article class="caixa">
                <h3>Display: inline vs block</h3>
                <p><span class="tag-inline">span inline </span>fica na linha,
                    enquanto elementos quebram linha.</p>
            </article>
        </section>

        <!--Seção Tabela-->
        <section id="tabela" class="card">
            <h2>Tabela de horários (exemplo)</h2>
            <table class="tabela">
                <thead>
                    <tr>
                        <th>Dia</th>
                        <th>Conteúdo</th>
                        <th>Duração</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Segunda</td>
                        <td>Estrutura HTML</td>
                    </tr>
                    <tr>
                        <td>Quarta</td>
                        <td>Seletores e Box Model</td>
                    </tr>
                    <tr>
                        <td>Sexta</td>
                        <td>Formulário e Responsivo</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!--Seção Formulário-->
        <section id="contato" class="card">
            <h2>Fale conosco</h2>
            <form action="#" class="formulario" method="post">
                <div class="grupo">
                    <label for="nome">Nome</label>
                    <input type="text" id="nome" name="nome" placeholder="Seu nome" required>
                </div>
                <div class="grupo">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" name="email" placeholder="seuemail@email.com" required>
                </div>
                <div class="grupo">
                    <label for="mensagem">Mensagem</label>
                    <textarea id="mensagem" name="mensagem" rows="5" placeholder="Escreva sua mensagem"></textarea>
                </div>
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>
     <!--Rodapé-->
    <footer class="rodape">
       <small>&copy; 2025 . Página didática para aula de HTML + CSS</small>



       //CSS

    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html, body {
    height: 100%;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', 
  Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  line-height: 1.5;
  background: #f6f7fb;
  color: #1f2937;
}

:root {
  --cor-primaria: #0ea5e9;
  --cor-secundaria: #f59e0b;
  --fundo-card: #ffffff;
  --borda-card: #e5e7eb;
  --fundo-tabela: #f1f5f9;
}

h1,
h2,
h3 {
 line-height: 1.2;
}

h1 {
    font-size: 2rem;
    margin: 0.2rem 0;
}

h2 {
    font-size: 1.5rem;
    margin: 0 0 0.5rem;
}

h3 {
    font-size: 1.125rem;
    margin: 0.5rem 0;
}

p {
 margin: 0.6rem 0;
}

a {
 color: var(--cor-primaria);
 text-decoration: none;
}

a:hover
a:focus {
  text-decoration: underline;
}

a:active {
  opacity: 0.8;
}

.topo {
  padding: 1rem;
  text-align: center;
  background: linear-gradient(180deg, rgba(14, 165, 233, 0.15), transparent);
}

.logo {
  width: 120px;
  height: 60px;
  background: var(--cor-primaria);
  color: var(--fundo-card);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  letter-spacing: 1px;
  border-radius: 6px;
  margin: 0 auto 0.5rem;
}

.subtitulo {
  color: #475569;
  margin-top: 0;
}

.menu {
  list-style: none;
  padding: 0;
  margin: 0.8rem 0 0;
  display: flex;
  gap: 0.75rem;
  justify-content: center;
}

.menu a {
  display: inline-block;
  padding: 0.5rem 0.8rem;
  border-radius: 0.5rem;
  background: var(--fundo-card);
  border: 1px solid #e5e7eb;
}

.menu a:hover {
    background: #f8fafc;
}

.container {
  max-width: 960px;
  margin: 1.2rem;
  padding: 0 1rem;
}

.card {
  background: var(--fundo-card);
  border: 1px solid var(--borda-card);
  padding: 1rem;
}
    </footer>
</body>
</html>
