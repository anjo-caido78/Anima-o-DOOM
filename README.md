# Anima-o-DOOM
Teste/Aula de DOOM
----------------------------------------------------------------------------------------------------------------------------------------------------------
Codigo HTML.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tela de Carregamento</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Tela de carregamento -->
    <div id="loading-screen">
        <div class="loader"></div>
        <p>Carregando...</p>
    </div>

    <!-- Conteúdo principal --> 
    <div id="content" class="hidden">
        <h1>Bem-vindo!</h1>
        <p>O conteúdo foi carregado com sucesso.</p>
        <button id="block01">Aperte AQUI</button>
        <button id="block02">Aperte aqui</button>
    </div>

    <script src="script.js"></script>
</body>
</html>

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Codigo  CSS.
/* Estilo da tela de carregamento */
#loading-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #2c3e50;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
    font-size: 20px;
    transition: opacity 0.5s ease;
}

/* Animação do spinner (loader) */
.loader {
    border: 8px solid #f3f3f3;
    border-top: 8px solid #3498db;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    animation: spin 1s linear infinite;
    margin-bottom: 20px;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Classe para esconder a tela de carregamento */
.hidden {
    opacity: 0;
    pointer-events: none; /* Impede interação com a tela escondida */
}

/* Estilo do conteúdo principal */
#content {
    padding: 20px;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
}

/* Estilo dos botões */
#block01, #block02 {
    padding: 10px 20px;
    font-size: 16px;
    color: #fff;
    background-color: #3498db;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: transform 0.3s ease;
}

/* Efeito de hover nos botões */
#block01:hover, #block02:hover {
    transform: scale(1.1);
    background-color: #2980b9;
}
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Codigo Javascript.
window.onload = function() {
    const loadingScreen = document.getElementById('loading-screen');
    const content = document.getElementById('content');

    // Simula um tempo de carregamento de 3 segundos
    setTimeout(function() {
        // Adiciona a classe 'hidden' para iniciar a transição
        loadingScreen.classList.add('hidden');

        // Mostra o conteúdo principal
        content.style.display = 'block';

        // Remove a tela de carregamento do DOM após a transição
        loadingScreen.addEventListener('transitionend', function() {
            loadingScreen.style.display = 'none';
        });
    }, 3000); // 3000 milissegundos = 3 segundos
};
