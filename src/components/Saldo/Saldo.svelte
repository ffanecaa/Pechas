<p>Es {saldo}</p>
{#if (saldo >0)}
💰
{/if}
{#if (saldo <0)}
👇
{/if}
{#if (saldo ===0)}
👌
{/if}




<script>
  export let saldo=0






</script>