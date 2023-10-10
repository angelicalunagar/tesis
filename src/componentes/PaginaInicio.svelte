<script>
import {Image} from 'sveltestrap';
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


<Container>
  <Row>
    <Col class="col1">
      <Row >
        <p id="titulo">
          Caracterización de una función usando la derivada
        </p>
      </Row>
      <Row >
        <Container id="contenedor_port1">
          <p id="port1_texto">Esta página web está pensada para que aprendas el concepto de derivada y su utilidad para caracterizar funciones. El objetivo es que aprendas con el mínimo de teoría, de forma intuitiva e interactiva para que las matemáticas dejen de ser aburridas y complicadas. 
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

<p id="párrafo_abajo" class="tit">Holaaa</p>

<style>
    @import "../../static/estilos.css";  
</style>