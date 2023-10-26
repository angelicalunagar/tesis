<script>
  import {
    Row,
    Col,
    Container,
    Carousel,
    CarouselControl,
    CarouselIndicators,
    CarouselItem
  } from 'sveltestrap';

  const items = [
    'est_1.jpg',
    'est_2.jpg',
    'est_3.jpg'
  ];
  let activeIndex = 0;
  //Atributos agregados a la etiqueta que se está creando
  export let titulo ="";
  export let texto = "";
  export let id="";
 

</script>


<Container class="contenedor" id={id}>
  <Row>
    <Col class="col1">
      <Row >
        <h2 class="tit">
          {titulo}
        </h2>
      </Row>
      <Row >
          <p class="caja-texto">
            {@html texto} 
          </p> 
      </Row>
    </Col>

    <Col>
      <Carousel {items} bind:activeIndex interval={3000}>
        <CarouselIndicators bind:activeIndex {items} />
        
      
        <div class="carousel-inner">
          {#each items as item, index}
            <CarouselItem bind:activeIndex itemIndex={index}>
              <img src={item} class="d-block" style="width: 95%; height: 30.2em; object-fit: cover;" alt={`${item} ${index + 1}`} />
            </CarouselItem>
          {/each}
        </div>
        
      
        <CarouselControl direction="prev" bind:activeIndex {items} />
        <CarouselControl direction="next" bind:activeIndex {items} />
      </Carousel>
    </Col>
  </Row>
  
</Container>

<style>
    @import "../../static/PaginaGeneral.css";
</style>