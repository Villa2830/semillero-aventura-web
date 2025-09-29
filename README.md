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
    
</body>
</html>
