<template>
  <!-- cartas -->
  <section class="container">
    <h1 class="text-center">La Casa del Sabor</h1>
    <div class="row">
      <div class="col-sm-8">
        <img
          src="https://images.unsplash.com/photo-1540189549336-e6e99c3679fe?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=800&q=60"
          style="max-height: 500px; text-align: end">
      </div>

      <div class="col-sm-4">
        <p>La Casa del Sabor es un encantador restaurante ubicado en el corazón de la ciudad, conocido por su ambiente
          acogedor y su exquisita cocina internacional. Fundado en 2020, La Casa del Sabor ha ganado rápidamente una
          reputación por sus platos creativos que combinan sabores tradicionales con un toque moderno. Nuestro equipo de
          chefs expertos utiliza solo los ingredientes más frescos y de la más alta calidad para crear una experiencia
          gastronómica inolvidable.

          El menú de La Casa del Sabor incluye una amplia variedad de opciones, desde entrantes ligeros hasta platos
          principales sustanciosos y postres decadentes. Ya sea que estés buscando un lugar para una cena romántica, una
          reunión familiar o una comida de negocios, La Casa del Sabor ofrece el ambiente perfecto para cualquier
          ocasión.</p>
      </div>
    </div>

    <h1 class="text-center">Nuestros Productos</h1>

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
    getImgProd(imgagen) {
      return require(`../assets/img/${imgagen}`)
    }
  },
}
</script>