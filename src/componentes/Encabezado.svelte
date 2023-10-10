<script>
  import {Image} from 'sveltestrap';
  import {
    Nav,
    NavItem,
    NavLink,
  } from 'sveltestrap';
</script>

<Nav class="encabezado" color="blue">
  <NavItem class="logo">
    <NavItem class="logo_item">
      <Image src="logo_cinves.png"/>
    </NavItem>
    <NavItem class="logo_item">
      <Image src="logo_matedu.png"/>
    </NavItem>
  </NavItem>
  <NavItem class="links">
    <NavItem>
      <NavLink href="#" class="nav-link">Inicio</NavLink>
    </NavItem>
    <NavItem>
      <NavLink href="#párrafo_abajo" class="nav-link">Quienes somos</NavLink>
    </NavItem>
    <NavItem>
      <NavLink href="#" class="nav-link">Contáctanos</NavLink>
    </NavItem>
    <NavItem>
      <NavLink href="/Aprende" color="success" class="nav-link">Aprende</NavLink>
    </NavItem>
  </NavItem>
</Nav>


<style>
  @import "../../static/estilos.css";
  
</style>
