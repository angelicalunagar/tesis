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
</script>


<Container class="comp" id="inicio">
  <Row>
    <Col class="col1">
      <Row >
        <p class="titulo">
          Caracterización de una función usando la derivada
        </p>
      </Row>
      <Row >
        <Container id="contenedor_pagInicio">
          <p class="texto_justif">Esta página web está pensada para que aprendas el concepto de derivada y su utilidad para caracterizar funciones. El objetivo es que aprendas con el mínimo de teoría, de forma intuitiva e interactiva para que las matemáticas dejen de ser aburridas y complicadas. 
          </p>
        </Container>
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
  @import "../../static/estilos.css";  
  :global(#contenedor_pagInicio){
  background-color: #FF821C;
  border-radius: 20px;
  padding: 2em 4em;
}
</style>