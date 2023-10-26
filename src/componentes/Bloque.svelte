<script>
  export let titulo="";
  export let subtitulo="";
  export let imagen="";
  export let descripcion_imagen="";
</script>

<div class="contenedor-bloque">
      
  <div class="texto-bloque">
    <p class="titulo-bloque"><b>{titulo}</b></p>
    <p class="subtitulo-bloque">{subtitulo}</p>
  </div>
  <div class="img-bloque">
    <img class="img" 
    src={`img_${imagen}.png`} alt={descripcion_imagen} />
  </div>

  <div class="boton-bloque">
    <button>
      Estudiar
    </button>
  </div>

</div>

<style>
  .contenedor-bloque{
  width: 15em;
  height: 85vh;
  margin: 10px 10px 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #011627;
  box-shadow: 0 3px 13px 1px rgb(0 0 0 /9%);
}

.img-bloque{
  margin-top: 0;
  margin-bottom: 0;
  width: 90%;
  height: 43%;
  overflow: hidden;
}

.img{
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.texto-bloque{
  text-align: center;
  padding: 40px;
  font-family: Lato, sans-serif;
  font-weight: 400;
  line-height: 1.5rem;
  height: 35%;
  margin-top: 0;
  margin-bottom: 0;
} 

.titulo-bloque{
  font-size: 1.3rem;
  color: #FF821C;
  margin-top: 0;
  margin-bottom: 0;
}

.subtitulo-bloque{
  margin-top: 0;
  margin-bottom: 0;
  font-size: 1.3rem;
  margin-top: 15px;
  padding-bottom: 30px;
  text-align: center;
  color: #fff;
}

.boton-bloque{
  height: 8%;
}

@media screen and (min-width: 601px) and (max-width: 1025px ){
  .contenedor-bloque{
    width: 40%;
    height: 100%;
  } 
  
  .subtitulo-bloque{
    font-size: 2rem;
    line-height: 1.8rem;
  }
}

@media screen and (max-width: 600px){
  .contenedor-bloque{
    width: 75%;
    height: 80%;
  } 
}
</style>