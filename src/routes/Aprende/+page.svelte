<script>
	import Bloque from "../../componentes/Bloque.svelte";
  import Encabezado from "../../componentes/Encabezado.svelte";
</script>


<div class="fondo-azul">
  <Encabezado/>
<div class=contenedor-bloques>
  <Bloque
    titulo="BLOQUE 1" 
    subtitulo="Funciones"
    imagen="bloque1"
    descripcion_imagen="Funciones"/>
  <Bloque
    titulo="BLOQUE 2" 
    subtitulo="Construcción de la derivada de una función"
    imagen="bloque2"
    descripcion_imagen="Derivada"/>
  <Bloque
    titulo="BLOQUE 3" 
    subtitulo="Crecimiento, decrecimiento, máximos y mínimos de una función"
    imagen="bloque3"
    descripcion_imagen="Máximos y mínimos"/>
  <Bloque
    titulo="BLOQUE 4" 
    subtitulo="Concavidad, segunda derivada y puntos de inflexión"
    imagen="bloque4"
    descripcion_imagen="Concavidad y puntos de inflexión de una función"/>
  <Bloque
    titulo="BLOQUE 5" 
    subtitulo="Práctica interactiva para caracterizar una función usando la primera y segunda derivada."
    imagen="bloque5"
    descripcion_imagen="Estudiante practicando en la computadora"/>
</div>
</div>



<style>
  .contenedor-bloques{
    height: 100%;
    min-height: 600px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

.fondo-azul {
    font-family: Raleway;
    font-size: medium;
    padding-top: 8.2em;
}

</style>
