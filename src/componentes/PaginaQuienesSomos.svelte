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
  
  
  <Container class="comp" id="quienes_somos">
    <Row>
      <Col class="col1">
        <Row >
          <p class="titulo">
            ¿Quiénes somos?
          </p>
        </Row>
        <Row >
          <Container id="contenedor_quienesSomos">
            <p class="texto_justif" id="texto_quienesSomos">
              Somos un grupo de investigadores del Departamento de
              Matemática Educativa del Centro de Investigación
              y de Estudios de Posgrado del IPN. Actualmente
              estudiamos el impacto de las tecnologías digitales
              en la enseñanza y el aprendizaje de las
              matemáticas para modificar el currículum y la 
              manera de enseñar.
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
    :global(#contenedor_quienesSomos){
      background-color: #7D0D1A;
      border-radius: 20px;
      padding: 2em 4em;
    }
    :global(#texto_quienesSomos){
      color: white;
    } 
  </style>