<template>
  <div id=news>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-12"
        v-for="(movie, index) of movies"
        :key="index"
      >
        <div class="d-flex justify-content-center align-items-center">
          <div class="p-3">
            <img :src="movie.Poster" alt="movie poster" />
          </div>

          <div class="p-2">
            <h2>
              <b>{{ movie.Title }}</b>
            </h2>
            <hr />
            <h6><b>Genero: </b>{{ arrayGenero[index] }}</h6>
            <p class="text-justify">
              <b>{{ arrayTitulosespañol[index] }} : </b
              >{{ arrayResumen[index] }}
            </p>
            <h6><b>Año: </b>{{ movie.Year }}</h6>
          </div>
        </div>

        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
          <a
            :href="arrayYoutube[index]"
            class="btn btn-outline-info"
            target="_blank"
            >Tráiler</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      movies: null,
      arrayResumen: [
        "Cal Weaver está viviendo el sueño americano. Él tiene un buen trabajo, una casa preciosa, niños excelentes y una esposa hermosa, llamada Emily. Sin embargo, la aparente vida perfecta de Cal se derrumba cuando descubre que Emily le ha sido infiel y quiere divorciarse. Ahora, con más de 40 años, e inesperadamente soltero, Cal ingresa al vicioso mundo de las citas románticas. Jacob Palmer decide ayudar a Cal y le enseña a tener éxito con las damas.",
        "Un general demente que cree que los comunistas planean dominar el mundo ordena bombardear la Unión Soviética, iniciando una guerra nuclear. Al mismo tiempo, el presidente y sus asesores del Pentágono intentan detener el proceso.",
        "Las vidas de varias parejas se entrecruzan en Londres, poco antes de la Navidad, con resultados románticos, divertidos y agridulces.",
        "El joven William Shakespeare se enamora de Viola, lo que despierta su creatividad, pero ella es la prometida de Wessex.",
      ],
      arrayTitulosespañol: [
        "Loco y estúpido amor",
        "Dr. Insólito o: cómo aprendí a dejar de preocuparme y amar la bomba",
        "Realmente amor",
        "Shakespeare apasionado",
      ],
      arrayGenero: [
        "Romance/Comedia",
        "Comedia/Bélico",
        "Romance/Drama",
        "Romance/Drama",
      ],
      arrayYoutube: [
        "https://www.youtube.com/watch?v=gu12MnF2-W4",
        "https://www.youtube.com/watch?v=8McYkfVm8sc",
        "https://www.youtube.com/watch?v=ZovXem-Giog",
        "https://www.youtube.com/watch?v=v5R5La5f3eo",
      ],
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=love&type=movie&apikey=23daade9")
      .then((response) => {
        this.movies = response.data.Search.slice(0, 4);
        console.log(this.movies);
      });
  },
};
</script>
<style scoped>
</style>

