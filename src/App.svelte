
<h1 class="texto"> PECHAS<span>SSS</span></h1>
<main class="appSvelte">
  <label class="texto" >
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
     <td>NOMBRE: <span> { usuario.nombre}  </span> </td>
   <td>ENTREGA:  <span>  {usuario.aporte}  </span> </td>
   <td>SALDO: <span>  {(usuario.aporte)-cadaUsuario}  </span> </td>    <!-- lo que me convendria pasar a saldo  -->
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

table:nth-child(even){
  background-color: #938c3147;
  font-size: 1.2rem;
  color:white;
}
table:nth-child(odd){
  background-color: #eb250b2f;;
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
.texto {
    display: inline-block;
    font-size: 5em;
  
    
}

.texto span {
    display: inline-block;
    transform-origin: 50% 50%;
    animation: distorsion 20s ease-in-out infinite;
}

@keyframes distorsion {
    0% {
        transform: translateZ(0) rotateY(0) rotateX(0);
    }
    50% {
        transform: translateZ(100px) rotateY(180deg) rotateX(180deg);
    }
    100% {
        transform: translateZ(0) rotateY(360deg) rotateX(360deg);
    }
}
  td{
    font-weight: 600;
    color:#938c31;
    text-shadow: 1px 1px 2px white;
    font-size: 1.6rem;
   
  }
  td span{
    color: #eb250bc3;
    font-weight: 900;
    font-size: 1.6rem;
    text-shadow: 1px 1px 2px white;
    text-transform: uppercase;
   
  }
  
  
</style> 