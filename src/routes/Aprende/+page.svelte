<script lang="ts">
  import {Styles} from 'sveltestrap';
  import {
    Button,
    Card,
    CardBody,
    CardFooter,
    CardHeader,
    CardSubtitle,
    CardText,
    CardTitle,
    Image
  } from 'sveltestrap';
</script>

<div class="column">
  <Card class="mb-3">
    <CardHeader>
      <CardTitle>BLOQUE 1</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle class=cont_subtitulo>Funciones</CardSubtitle>
      <CardText>
        <Image src="img_bloque1.jpg"/>
      </CardText>
      <Button>Button</Button>
    </CardBody>
    <CardFooter>Footer</CardFooter>
  </Card>

</div>
<div class="column">
  <Card class="mb-3">
    <CardHeader>
      <CardTitle>BLOQUE 2</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle class=cont_subtitulo>Construcción de la derivada de una función
      </CardSubtitle>
      <CardText>
        <Image src="img_bloque2.png"/>
      </CardText>
      <Button>Button</Button>
    </CardBody>
    <CardFooter>Footer</CardFooter>
  </Card>
</div>
<div class="column">
  <Card class="mb-3">
    <CardHeader>
      <CardTitle>BLOQUE 3</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle class=cont_subtitulo>Crecimiento, decrecimiento, máximos y mínimos de una función
      </CardSubtitle>
      <CardText>
        <Image src="img_bloque3.png"/>
      </CardText>
      <Button>Button</Button>
    </CardBody>
    <CardFooter>Footer</CardFooter>
  </Card>
</div>
<div class="column">
  <Card class="mb-3">
    <CardHeader>
      <CardTitle>BLOQUE 4</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle class=cont_subtitulo>
        Concavidad
        <br>
        Segunda derivada
        <br>
        Puntos de inflexión
        </CardSubtitle>
      <CardText>
        <Image src="img_bloque4.png"/>
      </CardText>
      <Button>Button</Button>
    </CardBody>
    <CardFooter>Footer</CardFooter>
  </Card>
</div>
<div class="column">
  <Card class="mb-3">
    <CardHeader>
      <CardTitle>BLOQUE 5</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle class=cont_subtitulo>Práctica interactiva para caracterizar una función usando la primera y segunda derivada.
      </CardSubtitle>
      <CardText>
        <Image src="img_bloque5.png"/>
      </CardText>
      <Button>Button</Button>
    </CardBody>
    <CardFooter>Footer</CardFooter>
  </Card>
</div>


<Styles />

<style>
  @import "../../../static/estilos.css";
  .column{
    width: 19%;
    float: left;
    padding: 3em;
    box-sizing: border-box;
    background-color: white;
    margin-right: 0.5em;
    margin-top: 2em;
  } 
</style>
