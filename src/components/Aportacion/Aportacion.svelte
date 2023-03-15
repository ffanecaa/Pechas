

<main>
    <label >nombre
        <input type="text" bind:value={nombre}>
    </label>
    <label >aportacion
        <input type="number" bind:value={aportadoPorPersona}>
    </label>
    <button on:click ={manexador}>Añadir</button>
    <p>{numeroParticipantes}</p>
</main>
<!-- <Saldo  bind:saldo={saldo}/> -->

<script>
 import Saldo from "../Saldo/Saldo.svelte";
 export let arrayParticipantes =[]
 export let totalGasto
// export let saldo
let loQueQueda
 let numeroParticipantes=0
let clase
let nombre=""
export let aportadoPorPersona =0 
 export let cadaUsuario


function manexador (){
   let usuarios = [...arrayParticipantes]
   usuarios.push(clase)
   arrayParticipantes=usuarios
}
$:cadaUsuario= (totalGasto/numeroParticipantes)

$:{numeroParticipantes =arrayParticipantes.length}
$:{
    clase= {
        nombre:nombre,
        aporte:aportadoPorPersona
        

    }
}



</script>