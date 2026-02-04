#HTML

<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>SENAIFLIX - Filmes e Séries</title>
    <link rel="stylesheet" href="home.css" />
    <link rel="stylesheet" href="../assets/styles/global.css">
  </head>
  <body>
    <header class="cabecalho">
      <a href="index.html">SENAIFLIX</a>
      <img id="menu-btn" class="hamburger-menu" src="../assets/icons/material-symbols_menu (1).png" alt="">
      <nav>
        <a href="#">Início</a>
        <a href="#titulo-filmes">Filmes</a>
        <a href="#titulo-series">Séries</a>
      </nav>
      <nav class="menu-mobile" id="menu-mobile">
        <a href="#">Início</a>
        <a href="#titulo-filmes">Filmes</a>
        <a href="#titulo-series">Séries</a>
      </nav>
    </header>
    <main>
      <section class="banner">
        <div class="div-banner">
          <h2>Assista agora!</h2>
          <p>
            Ao saber que tem câncer, um professor passa a fabricar metanfetamina
            pelo futuro da família, mudando o destino de todos.
          </p>
        </div>
      </section>
      <div class="inputs">
        <div class="pesquisa">
          <label for="pesquisar">Pesquise por filmes e/ou séries:</label>
          <input type="text" placeholder="Insira um título" id="pesquisar" />
        </div>

        <div class="filtro">
          <label for="genero">Filtrar por gênero:</label>
          <select name="genero" id="genero">
            <option selected value="">Selecione um gênero</option>
            <option value="Drama">Drama</option>
            <option value="Romance">Romance</option>
            <option value="Terror">Terror</option>
            <option value="Ficção científica">Ficção científica</option>
            <option value="Thriller">Thriller</option>
            <option value="Ação">Ação</option>
            <option value="Comédia">Comédia</option>
            <option value="Animação">Animação</option>
            <option value="Aventura">Aventura</option>
            <option value="Crime">Crime</option>
            <option value="Fantasia">Fantasia</option>
            <option value="Mistério">Mistério</option>
            <option value="Sci-Fi & Fantasy">Sci-Fi & Fantasy</option>
          </select>
          <button id="limpar-filtro" class="limpar-filtros">Limpar filtros</button>
        </div>
      </div>
      <section class="filmes-series">
        <h2 id="titulo-filmes">Filmes</h2>
        <div id="filmes-container" class="card-container">
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
        </div>
      </section>
      <section class="filmes-series">
        <h2 id="titulo-series">Séries</h2>
        <div id="series-container" class="card-container">
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
          <a href="../detalhes-do-filme/index.html" class="card"></a>
        </div>
      </section>
    </main>
    <footer>
      <p>Nos sigam nas redes sociais</p>
      <div class="imgs">
        <img src="../assets/imgs/mdi_twitter.svg" alt="Logo do Twitter" />
        <img
          src="../assets/imgs/ri_instagram-fill.svg"alt="Logo do Instagram"/>
        <img src="../assets/imgs/mdi_youtube.svg" alt="Logo do Youtube" />
      </div>
    </footer>
  </body>

  <script src="../scripts/script.js"></script>
</html>




#CSS

.banner {
    background-image: url("../assets/imgs/Banner-BB.png");
    background-repeat: no-repeat;
    background-size: cover;
    height: 700px;

    display: flex;
    align-items: center;
    padding: 0 80px;
}

.div-banner {
    display: flex;
    flex-direction: column;
    max-width: 480px;
    gap: 20px;
}

.div-banner p {
    font-size: 1.5em;
}

.div-banner h2 {
    font-size: 2.5em;
}

main {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.inputs {
    display: flex;
    align-items: center;
    padding: 50px;
    gap: 100px;
}

.filtro, .pesquisa  {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
}

button {
    text-align: center;
    font-size: 0.8em;
    padding: 5px;
}

button, input, select {
    height: 30px;
    width: 250px;

    background-color: #000000;
    border-radius: 7px;
    border: 1px solid #ffffff;
    padding: 5px;
    color: #ffffff;
}

.filmes-series {
    padding: 50px;
}

.filmes-series h2{
    font-size: 1.5em;
}

.card-container {
    width: 100%;
    height: auto;
    margin-top: 10px;

    display: flex;
    gap: 20px;
}

.card {
    height: 180px;
    width: 120px;

    background-image: url("../assets/imgs/eassimqueacaba.webp");
    background-size: cover;
    margin-right: 10px;
    border-radius: 7px;
}

.menu-mobile{
    display: none;
}

/* RESPONSIVIDADE */
@media (max-width: 1023px){

    .inputs {
        flex-direction: column;
        gap: 25px;
    }

    .inputs label {
        flex-direction: column;
        align-items: flex-start;
        width: 100%;
        gap: 8px;
    }

    .inputs input,
    .inputs select,
    .inputs button,
    .pesquisa {
        width: 100%;
        height: 40px;
    }

    .filtro {
        flex-direction: column;
        width: 100%;
        gap: 15px;
    }

    .card-container {
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        gap: 15px;
        margin-top: 40px;
    }

    .card {
        width: 40%;
        height: auto;
        aspect-ratio: 2 / 3;
    }

    .menu-mobile {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 60px;
        right: 10px;
        background: #111;
        padding: 15px;
        border-radius: 5px;
    }
    
    .menu-mobile a {
        color: white;
        text-decoration: none;
        margin: 10px 0;
    }
    

}

@media (max-width: 768px){
    .banner {
        height: 450px;
        padding: 0 20px;
        background-position: center top;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .div-banner{
        max-width: 80%;
        align-items: center;
    }

    .div-banner h2 {
        font-size: 2em;
    }

    .div-banner p {
        font-size: 1.1em;
    }

    .filmes-series {
        padding: 30px 20px;
    }

    .filmes-series h2{
        margin-left: 10%;
        margin-bottom: 20px;
    }

    .card-container{
        flex-direction: column;
        align-items: center;
    }

    .card {
        width: 80%;
    }
}
