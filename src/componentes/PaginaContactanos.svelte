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
  <Container class="comp" id="contactanos">
    <Row>
      <Col class="col1">
        <Row >
          <p class="titulo">
            Contáctanos
          </p>
        </Row>
        <Row >
          <Container class="texto_contactanos">
            <p class="texto_justif">
              Si tuvieras alguna duda o sugerencia sobre el proyecto,
              no dudes en ponerte en contacto con nosotros:
              <br>
              Angélica Luna García
              <br>
              angelica.luna@cinvestav.mx 2221754139 
              <br>
              Hugo  Rogelio Mejía Velasco
              <br>
              hmejia@cinvestav.mx   (52)+(55) 57473800 extensión 6013
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
    :global(.texto_contactanos){
      background-color: #2EC4B6;
      border-radius: 20px;
      padding: 2em 4em;
    }
    :global(#port_texto1){
      color: white;
    } 
    :global(#contactanos){
      margin-bottom: 0.5em;
    }
  </style>