
<script>
let coins = [];

  const loadCoins = async () => {
    const res = await fetch(
      `http://www.claudiovm.somee.com/api/AccesoTodos`
    );
    const data = await res.json();
    console.log(data);

    coins = data;

  };

  loadCoins();
</script>

<h1>Hola</h1>

{#each coins as coin, i}
   {coin.username}
   <br>
{/each}

