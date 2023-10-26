<script>
  import Encabezado from "../componentes/Encabezado.svelte";
  import {Styles} from 'sveltestrap';
	import PaginaGeneral from "../componentes/PaginaGeneral.svelte";
	import { each } from "svelte/internal";
  
  let titulos=["Caracterización de una función usando la derivada", 
  "¿Quiénes somos?", 
  "Contáctanos"];

  let textos=["Esta página web está pensada para que aprendas el concepto de derivada y su utilidad para caracterizar funciones. El objetivo es que aprendas con el mínimo de teoría, de forma intuitiva e interactiva para que las matemáticas dejen de ser aburridas y complicadas.",
  "Somos un grupo de investigadores del Departamento de Matemática Educativa del Centro de Investigación y de Estudios de Posgrado del IPN. Actualmente estudiamos el impacto de las tecnologías digitales en la enseñanza y el aprendizaje de las matemáticas para modificar el currículum y la manera de enseñar.",
  "Si tuvieras alguna duda o sugerencia sobre el proyecto,no dudes en ponerte en contacto con nosotros: <br> Angélica Luna García <br> angelica.luna@cinvestav.mx 2221754139 <br> Hugo  Rogelio Mejía Velasco <br> hmejia@cinvestav.mx   (52)+(55) 57473800 extensión 6013"];
  let ids =["inicio", "quienesSomos", "contactanos"];
  let bgColores=["#FF821C", "#7D0D1A", "#2EC4B6"];
  let colorTexto=["black", "#FDFFFC", "black"];
  let arreglo=[0, 1, 2];

</script>


<Styles/>
<div class="fondo-azul">
  <Encabezado/>
{#each arreglo as ind}
  <PaginaGeneral 
  titulo={titulos[ind]} 
  texto={textos[ind]} 
  id={ids[ind]}  
  --bgcolor={bgColores[ind]}
  --color={colorTexto[ind]}/>  
{/each}

<!--   <PaginaGeneral 
    titulo={titulos[0]} 
    texto={textos[0]} 
    id={ids[0]} 
    --bgcolor={bgColores[0]}
    --color={colorTexto[0]}/>
  <PaginaGeneral 
    titulo={titulos[1]} 
    texto={textos[1]} 
    id={ids[1]} 
    --bgcolor={bgColores[1]}
    --color={colorTexto[1]}/>
  <PaginaGeneral 
    titulo={titulos[2]} 
    texto={textos[2]} 
    id={ids[2]}  
    --bgcolor={bgColores[2]}
    --color={colorTexto[2]}/> -->  
</div>

<style>
  .fondo-azul {
    background-color:#011627;
    font-family: Raleway;
    font-size: medium;
  }
</style>












