

<main>
  <label >
  gasto
  <input type="number" bind:value={totalGasto}>
  </label> 
</main>



<Aportacion 
          bind:totalGasto={totalGasto}
          bind:arrayParticipantes={recorrerArray}
          bind:cadaUsuario ={cadaUsuario}
          bind:aportadoPorPersona ={aportadoPorPersona}
          />
          <!-- bind:saldo={saldo}/> -->
          
  {#each recorrerArray as usuario}
  <table><tr>
     <td>nombre:{ usuario.nombre}</td>
   <td>entrega:{usuario.aporte}</td>
   <td>saldo:{(usuario.aporte)-cadaUsuario}</td>
  
  
  
 </tr>
 </table>
 icono<Saldo saldo={pasta}/>
   {/each} 


<script>
let aportadoPorPersona
  let totalGasto
  let cadaUsuario
  let aporte=[]
  let pasta
let recorrerArray=[]
import Aportacion from "./components/Aportacion/Aportacion.svelte";
import Saldo from "./components/Saldo/Saldo.svelte";



 $:pasta=aportadoPorPersona-cadaUsuario




</script>