<template>
  <div>
      <menu-principal></menu-principal>

    <div id="mycarousel" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-taget="#mycarousel" data-slide-to="0" class="active"></li>
        <li data-taget="#mycarousel" data-slide-to="1"></li>
        <li data-taget="#mycarousel" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div
          class="carousel-item active"
          style="background-image: url(./bannerimagenes/zombie.jpg)">
          <div class="container">
            <h1>Estación Zombie 2 : Península</h1>
            <p>
             Cuatro años después de la epidemia zombi, Corea sigue infestada de monstruos 
             y el soldado Jung-seok, que escapó del país, se ve obligado a regresar a Seúl 
             para recuperar un objeto valioso. Allí descubre que hay, todavía, personas sanas en la ciudad.
            </p>
          </div>
        </div>
        <div class="carousel-item" style="background-image: url(./bannerimagenes/tenet.jpg)">
          <div class="container">
            <h1>Tenet</h1>
            <p>
              Una acción épica que gira en torno al espionaje internacional,
              los viajes en el tiempo y la evolución, en la que un agente secreto debe prevenir 
              la Tercera Guerra Mundial.
            </p>
          </div>
        </div>
        <div
          class="carousel-item"
          style="background-image: url(./bannerimagenes/jovenesbrujas.jpg)">
          <div class="container">
            <h1>Jóvenes brujas: Nueva hermandad</h1>
            <p>
              Cuatro adolescentes aspirantes a brujas obtienen más de lo que 
              esperaban y van a aprovechar sus nuevos poderes.
            </p>
          </div>
        </div>
      </div>
      <a
        href="#mycarousel"
        class="carousel-control-prev"
        role="button"
        data-slide="prev"
      >
        <span class="sr-only">Previous</span>
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      </a>
      <a
        href="#mycarousel"
        class="carousel-control-next"
        role="button"
        data-slide="next"
      >
        <span class="sr-only">Previous</span>
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
      </a>
    </div>
  </div>
</template>

<script>
import MenuPrincipal from './MenuPrincipal';
export default {
  name: "BannerPrincipal",
  components: {
    MenuPrincipal,
    }
};
</script>

<style scoped>
.carousel-item {
  height: 25rem;
  background: #777;
  color: white;
  position: relative;
  background-position: center;
  background-size: cover;
}

.container {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding-bottom: 50px;
}
</style>
