<template>
  <!-- cartas -->
  <section class="container" id="productos">
    <h1 class=" text-center">Nuestros Productos</h1>

    <div class="row">
      <div class="col-sm-4 col-12 px-5 mb-4" v-for="(producto, i) in productos" :key="i">
        <!-- primera -->
        <div class="card">
          <img :src="getImgProd(imgProd[i])" class="card-img-top" alt="colaciones" />
          <div class="card-body">
            <h5 class="card-title fw-bold">{{ producto }}</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Dapibus ac facilisis in</li>
            <li class="list-group-item">Vestibulum at eros</li>
          </ul>
          <div class="card-body">
            <a href="#" class="card-link">Ver más</a>
            <a href="#" class="card-link">Comprar</a>
          </div>
        </div>
      </div>

      <router-link to="/">Volver al Home</router-link>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      productos: ['Bebidas', 'Colaciones', 'Desayunos', 'Dulces', 'Empanadas', 'Verduras'],
      imgProd: ['bebidas.jpg', 'colaciones.jpg', 'desayunos.jpg', 'dulces.jpg', 'empanadas.jpg', 'verduras.jpg']
    }
  },
  methods: {
    getImgProd(imgagen){
      return require(`../assets/img/${imgagen}`)
    }
  },
}
</script>