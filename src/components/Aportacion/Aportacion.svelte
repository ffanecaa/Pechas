

<main class="aportacion">
    <label >Nombre
        <input type="text" bind:value={nombre}>
    </label>
    <label >Aportacion
        <input type="number" bind:value={aportadoPorPersona}>
    </label>
    <button on:click ={manexador}>Añadir</button>
    <p>Participantes {numeroParticipantes}</p>
</main>

<script>

 let numeroParticipantes=0
 let clase
 let nombre=""
 export let aportadoPorPersona =0 
 export let cadaUsuario
 export let arrayParticipantes =[]
 export let totalGasto

/* guardo obx en array*/
function manexador (){
   let usuarios = [...arrayParticipantes]
   usuarios.push(clase)
   arrayParticipantes=usuarios
}

/* calcculo lo que tiene q pagar cada uno, al que se van agregando participantes*/
$:cadaUsuario= (totalGasto/numeroParticipantes)
/* hayo el numero de participantes se van agregando */
$:{numeroParticipantes =arrayParticipantes.length}

/* creo el boxecto */
$:{
    clase= {
        nombre:nombre,
        aporte:aportadoPorPersona
    }
}



</script>

<style>
  


</style>