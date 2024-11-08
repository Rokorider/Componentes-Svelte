<script>
    let isDark = true;

    function changeMode() {
        isDark = !isDark;
    }
</script>

<div id="contenedor" class:dark-mode={isDark} class:light-mode={!isDark}>
    <button on:click={changeMode}> 
        Cambiar a modo {isDark ? 'Claro' : 'Oscuro'}
    </button>

    <h1>Este es un ejemplo de tema {isDark ? 'Oscuro' : 'Claro'}</h1>
</div>

<style>

    .dark-mode {
        background-color: black;
        color: white;
    }

    .light-mode {
        background-color: white;
        color: black;
    }

    /* Botón en ambos modos */
    button {
        margin-top: 10px;
        padding: 8px 12px;
        font-size: 16px;
        border: none;
        cursor: pointer;
    }

    .dark-mode button {
        background-color: white;
        color: black;
    }

    .light-mode button {
        background-color: black;
        color: white;
    }
</style>
