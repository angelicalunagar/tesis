<script>
  import Encabezado from "../componentes/Encabezado.svelte";
  import PaginaInicio from "../componentes/PaginaInicio.svelte";
  import {Styles} from 'sveltestrap';
	import PaginaQuienesSomos from "../componentes/PaginaQuienesSomos.svelte";
  import PaginaContactanos from "../componentes/PaginaContactanos.svelte";
  import PaginaGeneral from "../componentes/PaginaGeneral.svelte";
  
  let titulos=["Caracterización de una función usando la derivada", 
  "¿Quiénes somos?", 
  "Contáctanos"];

  let textos=["Esta página web está pensada para que aprendas el concepto de derivada y su utilidad para caracterizar funciones. El objetivo es que aprendas con el mínimo de teoría, de forma intuitiva e interactiva para que las matemáticas dejen de ser aburridas y complicadas.",
  "Somos un grupo de investigadores del Departamento de Matemática Educativa del Centro de Investigación y de Estudios de Posgrado del IPN. Actualmente estudiamos el impacto de las tecnologías digitales en la enseñanza y el aprendizaje de las matemáticas para modificar el currículum y la manera de enseñar.",
  "Si tuvieras alguna duda o sugerencia sobre el proyecto,no dudes en ponerte en contacto con nosotros: <br> Angélica Luna García <br> angelica.luna@cinvestav.mx 2221754139 <br> Hugo  Rogelio Mejía Velasco <br> hmejia@cinvestav.mx   (52)+(55) 57473800 extensión 6013"];
</script>

<Styles/>
<Encabezado/>
<div class="separacion">
  <!-- <PaginaInicio/> -->
  <PaginaGeneral titulo={titulos[0]} texto={textos[0]} id="general"/>
</div>
<div class="separacion">
  <!-- <PaginaQuienesSomos/> -->
  <PaginaGeneral titulo={titulos[1]} texto={textos[1]} id="quienesSomos"/>
</div>

<PaginaGeneral titulo={titulos[2]} texto={textos[2]} id="contactanos"/>


<style>
  @import "../../static/estilos.css"; 
</style>











