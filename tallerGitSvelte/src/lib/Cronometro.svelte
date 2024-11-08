<script>
    let time = 0;
    let interval;
    let isRunning = false;

    function startTimer() {
        if (isRunning) return;
        isRunning = true;
        interval = setInterval(() => {
            time += 1;
        }, 1000);
    }
    function pauseTimer() {
        isRunning = false;
        clearInterval(interval);
    }
    function resetTimer() {
        isRunning = false;
        clearInterval(interval);
        time = 0;
    }

</script>
<div>
    <p>Tiempo: {time} segundos</p>
    <button on:click={startTimer}>Iniciar</button>
    <button on:click={pauseTimer}>Pausar</button>
    <button on:click={resetTimer}>Reiniciar</button>

</div>