<script>
    let search = '';
    const items = ['Manzana', 'Pera', 'Sandía', 'Melón', 'Uvas' ]
    $: filtrarItems = () => 
        items.filter(item => item.toLowerCase().includes(search.toLowerCase())
    );
    
    </script>
    
    
    
    <div class="container">
        <h1>Buscador</h1>
        <!-- Llamamos al filtro en el buscador -->
        <input type="text" bind:value={search}>    
        <ul>
            {#each filtrarItems() as item}
                <li>{item}</li>
            {/each}
        </ul>    
    </div>