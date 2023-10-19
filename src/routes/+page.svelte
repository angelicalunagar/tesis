<script>
  import Encabezado from "../componentes/Encabezado.svelte";
  import PaginaInicio from "../componentes/PaginaInicio.svelte";
  import {Styles} from 'sveltestrap';
	import PaginaQuienesSomos from "../componentes/PaginaQuienesSomos.svelte";
  import PaginaContactanos from "../componentes/PaginaContactanos.svelte";
</script>

<Styles/>
<Encabezado/>
<div class="separacion">
  <PaginaInicio/>
</div>
<div class="separacion">
  <PaginaQuienesSomos/>
</div>
<PaginaContactanos/>

<style>
  @import "../../static/estilos.css"; 
</style>











