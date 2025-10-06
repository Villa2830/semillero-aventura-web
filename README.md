# semillero-aventura-web
Este es un repositorio para el semillero de AventuraWeb donde nos construiremos un pequeño juego que nos dará las bases del desarrollo Web
## Salomé Villa Londoño 
Esto lo personalizaremos luego

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Juegos Snake SV🍓</title>
</head>
<body>
    <header class="header">
        <h1>Mi Juego Fresita SV🍓</h1>
    </header>
    <section class="hud">
        <div class="stats">
            <div class="stat"><span>Puntage:</span> <span id="scoreBoard">0</span></div>
            <div class="stat"><span>Mejor:</span> <span id="bestBoard">0</span></div>
            <div class="stat"><span>Longitud</span> <span id="lengthBoard">0</span></div>
            <div class="stat"><span>Nivel</span> <span id="levelBoard">1</span></div>
            <div class="stat"><span>Velocidad</span> <span id="speedBoard">100ms</span></div>
            <div class="stat"><span>Tiempo</span> <span id="timeBoard">00:00</span></div>
        </div>
        <div class="controls">
            <div class="control-group">
                <label for="sizeSelect">Tamaño</label>
                <select id="sizeSelect">
                    <option value="10" selected>10x10</option>
                    <option value="12">12x12</option>
                    <option value="15">15x15</option>
                    <option value="20">20x20</option>
             </select>
            </div>

            <div class="controls">
                <div class="control-group">
                    <label for="speedSelect">Velocidad</label>
                    <select id="speedSelect">
                        <option value="150" selected>Lenta</option>
                        <option value="100">Normal</option>
                        <option value="70">Rapida</option>
                        <option value="50">Insana</option>  
                    </select>
                </div>
            </div>

            <div class="controls">
                <div class="control-group">
                    <label for="modeSelect">Modo</label>
                    <select id="modeSelect">
                        <option value="Walls" selected>Paredes</option>
                        <option value="wrap">Teletransportarse</option>
                    </select>
                </div>
            </div>

            <div class="controls">
                <div class="control-group">
                    <label for="skinSelect">Skin</label>
                    <select id="skinSelect">
                        <option value="classic" selected>Clásico</option>
                        <option value="neon">Neón</option>
                        <option value="retro">Retro</option>
                        <option value="mantrix">Matrix</option> 
                    </select>
                </div>
                <div class="controls">
                    <div class="control-group">
                        <label for="volumeSelect">Volumen</label>
                        <input type="range" id="volumeSlider" min="0" max="100" value="40">
        </div>
        <button id="start">Start 🍓</button>
        <button id="pouse">Pouse ❤️</button>
    </section>
    <div class="board"></div>
    <section class="help">
        <p>Instrucción sasasasasasasasasa</p>
    </section>
    <div id="gameOver" class="overlay">
        <div class="overlay-card">
            <h2>Game Over ☠️</h2>
            <p>Mejor Puntaje: <span id="fianlBest">0</span> </p>
            <P>pUNTAJE:  <span id="fianlScore">0</span> </P>
            <div class="overlay-actions">
                <button id="restart">Restart 💕</button> 
            </div>
            <p class="hint">Pulsa <kbd>R </kbd>Para reiniciar o <kbd>Enter </kbd>Para empezar nuevo juego</p>
        </div>
    </div>






    css

:root {
    --bg: #0b1020;
    --panel: #121a33;
    --grid-empty: #e3e773;
    --grid-food: #55e7e7;
    --accent: #f35a69;
    --text: #e8ecff;
    --muted: #9aa3c7;
    --shadow: 0 10px 30px rgba(0,0,0,0.35);
    /* Skins de la serpiente*/
    --snake-color-classic: #e3e773;
    --snake-color-neon: #9dff00;
    --snake-color-retro: #ffd166;
    --snake-color-matrix: #00ff95;

}

html, body {
    height: 100%;
    margin: 0;
    background: radial-gradient(1000px 600px at 50% -200px, #1a2250 0%, var(--bg) 40%);
    color: var(--text);
    display: flex;
    flex-direction: column;
    align-items: center;
}

.header {
    width: 100%;
    max-width: 680px;
    padding: 20px 16px 0;
    box-sizing: border-box;
}
h1 {
    margin: 10px 0 6px;
    letter-spacing: 1px;
}

hr {
    border: none;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
    background-color: #00ff95;
}

.hud {
    width: 100%;
    max-width: 680px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    padding: 12px 16px 0;
    box-sizing: border-box;


}

.stats {
    display: grid;
    grid-template-columns: repeat(3, auto);
    gap: 8px 16px;
    background: #f35a69;
    border: 1px solid #9aa3c7;
    border-radius: 10px;
    padding: 10px 12px;
    box-shadow: var(--shadow);
}

.stat span:first-child {
    color: var(--muted);
    margin-right: 4px;
}

.controls {
    display: flex;
    gap: 10px;
    align-items: center;
    flex-wrap: wrap;
}

.cintrol-group {
    display: flex;
    flex-direction: column;
    gap: 4px;
    background: #f35a69;
    border: 1px solid rgba(0,0,0,0,35);
    border-radius: 10px;
    padding: 6px 8px;
    box-sizing: var(--shadow);
}

.control-group label {
    color: var(--muted);
    font-size: 12px;
}

.cintrol-group select {
    background: var(--panel);
    border: 1px solid rgba(0,0,0,0,35);
    color: var(--text);
    border-radius: 8px;
    padding: 6px 8px;
    font-size: 14px;
    cursor: pointer;
}


    
    
</body>
</html>
