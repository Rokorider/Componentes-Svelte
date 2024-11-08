<script>
  let count = 0
  const increment = () => {

    if (count < 20) {
      count += 1
    }
  }

  const decrement = () => {
    if (count > 0) {
      count -= 1
    }
  }

</script>

<button on:click={increment}>
  Incrementar
</button>

<button on:click={decrement}>
  Decrementar
</button>

<button>
  count is {count}
</button>

