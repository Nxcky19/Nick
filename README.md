<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Time to Study Mor</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        #timer {
            font-size: 48px;
        }
    </style>
</head>
<body>
<FONT COLOR="black"><h1>Time to Study Mor </h1> </FONT>
<div id="timer">50:00
   
</div>
<button id="startButton" onclick="startTimer()">Iniciar</button>
<button id="pauseButton" onclick="pauseTimer()" style="display: none;">Pausa</button>
<button id="resetButton" onclick="resetTimer()" style="display: none;">Reiniciar</button>


<FONT COLOR="black"><h2>Hii Nicky today is a beautiful day to learn how to save lives, u got it bbygirl...</h2></FONT>


<style>
    /* Estilos para el carrusel */
    .carousel {
        display: flex;
        overflow-x: auto;
        scroll-snap-type: x mandatory;
        -webkit-overflow-scrolling: touch;
    }
    .item {
        flex: 0 0 auto;
        width: 100%;
        scroll-snap-align: start;
    }
    /* Estilos para el reproductor de música */
    .music-player {
        width: 100%;
       
        padding: 20px;
        box-sizing: border-box;
    }
    .music-player audio {
        width: 100%;
    }
</style>


<div class="carousel">
    <div class="item">
        <div class="music-player">
            <h2>X19X</h2>
    
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/56dHJTQQ8lMGgBegxfYVDM?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
         
        </div>
           </div>
 
    <div class="item">
        <div class="music-player">
            <h2>MOR</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/3js3vnaiDDghVu9ADH93Q5?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </div>
       </div>
    <div class="item">
        <div class="music-player">
            <h2>DUCATI</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/444LqH6QlvR62nY8Vxn37u?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </div>
       </div>
    <div class="item">
        <div class="music-player">
            <h2>LCLM</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/4hUQ4FB9GD5oDmw3XHIr0G?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </div>
    <div class="item">
        <div class="music-player">
            <h2>SHIBUYA</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/0kI46dzlikgAVpJ6LdkbJE?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </div>
    <div class="item">
        <div class="music-player">
            <h2>FERXXO PA</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/7pijRxgRaBirPz6wDaJIp9?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </div>
    <div class="item">
        <div class="music-player">
            <h2>THE LIGHT MOR</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/16ScBmKm5WA3RwvTqiQlJd?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </div>
    <div class="item">
        <div class="music-player">
            <h2>A VERY GOOD END</h2>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/0lgs2Sa82lyX89nBUWyUy6?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </div>
    <!-- Añadir más elementos según sea necesario -->
</div>


<script>
    function nextSlide() {
        const carousel = document.querySelector('.carousel');
        carousel.scrollBy({ left: carousel.offsetWidth, behavior: 'smooth' });
    }
</script>
<script>
    let timer;
    let minutes = 50;
    let seconds = 0;
    let isRunning = false;

    function startTimer() {
        if (!isRunning) {
            isRunning = true;
            document.getElementById("startButton").style.display = "none";
            document.getElementById("pauseButton").style.display = "inline";
            document.getElementById("resetButton").style.display = "none";
            timer = setInterval(updateTimer, 1000);
        }
    }

    function pauseTimer() {
        if (isRunning) {
            isRunning = false;
            document.getElementById("startButton").style.display = "inline";
            document.getElementById("pauseButton").style.display = "none";
            document.getElementById("resetButton").style.display = "inline";
            clearInterval(timer);
        }
    }

    function resetTimer() {
        isRunning = false;
        clearInterval(timer);
        document.getElementById("startButton").style.display = "inline";
        document.getElementById("pauseButton").style.display = "none";
        document.getElementById("resetButton").style.display = "none";
        minutes = 50;
        seconds = 0;
        updateTimer();
    }

    function updateTimer() {
        if (minutes === 0 && seconds === 0) {
            clearInterval(timer);
            isRunning = false;
            document.getElementById("startButton").style.display = "inline";
            document.getElementById("pauseButton").style.display = "none";
            document.getElementById("resetButton").style.display = "inline";
        } else {
            if (seconds === 0) {
                minutes--;
                seconds = 59;
            } else {
                seconds--;
            }
            const formattedMinutes = minutes < 10 ? "0" + minutes : minutes;
            const formattedSeconds = seconds < 10 ? "0" + seconds : seconds;
            document.getElementById("timer").textContent = `${formattedMinutes}:${formattedSeconds}`;
        }
    }
</script>
 
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        #video-background {
            position: fixed;
            top: 0;
            left: 0;
            min-width: 100%;
            min-height: 100%;
            z-index: -1;
        }
        #content {
            position: relative;
            z-index: 1;
            background: rgba(255, 255, 255, 0.7);
            padding: 20px;
        }
        #timer {
            font-size: 48px;
        }
    </style>


    <video id="video-background" autoplay muted loop>
        <source src="https://github.com/Nxcky19/Nick/blob/main/salo.mp4" type="video/mp4">

    </video>
   </body>
     
