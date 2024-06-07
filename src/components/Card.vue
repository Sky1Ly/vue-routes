<template>
  <!-- cartas -->
  <section class="container" id="productos">
    <h1 class=" text-center">{{nomProducto}}</h1>

    <div class="row">
      <div class="col-sm-4 col-12 px-5 mb-4">
        <!-- primera -->
        <div class="card">
          <img src="" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title fw-bold">{{  }}</h5>
            <p class="card-text">{{  }}</p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">{{  }}</li>
            <li class="list-group-item">{{  }}</li>
          </ul>
          <div class="card-body">
            <router-link to="/">Comprar</router-link>
          </div>
        </div>
      </div>

      <router-link to="/">Volver al Home</router-link>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    producto: {
      type: Object
    }
  },

  computed: {
    nomProducto() {
      return `Conozca nuestro producto: ${this.$route.params.entrada}`
    }
  }  
}
</script>