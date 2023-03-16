
<h1 class="h1"> PECHASS</h1>
<main class="appSvelte">
  <label >
 GASTO
  <input type="number" bind:value={totalGasto}>
  </label> 




<Aportacion 
          bind:totalGasto={totalGasto}
          bind:arrayParticipantes={recorrerArray}
          bind:cadaUsuario ={cadaUsuario}
          bind:aportadoPorPersona ={aportadoPorPersona}
          />
          <!-- bind:saldo={saldo}/> -->
          
  {#each recorrerArray as usuario}
  <table class='table'><tr>
     <td>Nombre: { usuario.nombre}</td>
   <td>Entrega: {usuario.aporte}</td>
   <td>saldo: {(usuario.aporte)-cadaUsuario}</td>    <!-- lo que me convendria pasar a saldo  -->
 <td> <Saldo saldo={(usuario.aporte)-cadaUsuario}/></td>
  
  
  
 </tr>
 </table>

   {/each} 
  </main>
   <!-- icono<Saldo bind:saldo={pasta}/> -->
<script>
let aportadoPorPersona
  let totalGasto
  let cadaUsuario
  // let aporte
  let pasta
let recorrerArray=[]
import Aportacion from "./components/Aportacion/Aportacion.svelte";
import Saldo from "./components/Saldo/Saldo.svelte";



  $:pasta = aportadoPorPersona-cadaUsuario




</script>

 <style>
  main{
    display:grid;
    
  
  

  }
table:nth-child(even){
  background-color: rgba(210, 69, 26, 0.218);
  font-size: 1.2rem;
  color:white;
}
table:nth-child(odd){
  background-color: rgba(110, 174, 197, 0.396);
  font-size: 1.2rem;
  color:white;
}
input {
  width: 300px;
  height: 60px;

 ;
}

label, input{
  font-size: 3rem;
  padding: 2px;
}
</style> 