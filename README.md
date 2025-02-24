# Anima-o-DOOM
Teste/Aula de DOOM
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
