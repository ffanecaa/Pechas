<!-- <p>Es {saldo}</p> -->
{#if (saldo >0)}
<i>💷</i>
{/if}
{#if (saldo <0)}
<i> 👎🏻 </i>
{/if}
{#if (saldo ===0)}
<i>👌🏻</i>
{/if}




<script>
  export let saldo=0
/*  $: {
  if(saldo >0 ) icono=f
} */

</script>

<style>
  i{
    font-size: 2rem;
  }

</style>