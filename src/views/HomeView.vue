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

    <h1 class="text-center" id="productos">Nuestros Productos</h1>

    <div class="row">
      <div class="col-sm-4 col-12 px-5 mb-4" v-for="(producto, i) in productos" :key="i">
        <!-- primera -->
        <div class="card">
          <img :src="producto.imagen" class="card-img-top" alt="colaciones" />
          <div class="card-body">
            <h5 class="card-title fw-bold">{{ producto.nombre }}</h5>
            <p class="card-text">{{ producto.descripcion }}</p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Precio: {{producto.precio}}</li>
            <li class="list-group-item">Cantidad: {{producto.cantidad}}</li>
          </ul>
          <div class="card-body">
            <router-link :to="{path: enrutarProducto(producto.nombre), props: {producto}}" class="card-link">Ver Producto</router-link>
            <a href="#" class="card-link">Comprar</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  //enrutarProducto(producto.nombre)
  data() {
    return {
      productos: [
        {
          imagen: require('../assets/img/bebidas.jpg'),
          nombre: 'Bebidas',
          descripcion: 'Gran variedad de bebidas, desde bebidas personales, hasta bebidas en lata y familiares',
          precio: 'Desde $400 hasta $3.000',
          cantidad: 'Personal o Familiar'
        },
        {
          imagen: require('../assets/img/colaciones.jpg'),
          nombre: 'Colaciones',
          descripcion: 'Colación con un delicioso platillo de carne, atun, ensalada y postre',
          precio: 'Desde los $6.000',
          cantidad: 'Personal'
        },
        {
          imagen: require('../assets/img/desayunos.jpg'),
          nombre: 'Desayunos',
          descripcion: 'Delicioso desayuno con huevo y tostada frescos',
          precio: 'Desde los $3.000',
          cantidad: 'Personal'
        },
        {
          imagen: require('../assets/img/dulces.jpg'),
          nombre: 'Dulces',
          descripcion: 'Gran variedad de dulces, todos de 100 unidades',
          precio: 'Desde los $4.000',
          cantidad: '100 unidades'
        },
        {
          imagen: require('../assets/img/empanadas.jpg'),
          nombre: 'Empanadas',
          descripcion: 'Deliciosas empanadas de carne, pollo, perro y gato',
          precio: 'Desde los $5.000',
          cantidad: '1 docena'
        },
        {
          imagen: require('../assets/img/verduras.jpg'),
          nombre: 'Verduras',
          descripcion: 'Verduras frescas a tan solo un clic de distancia',
          precio: 'Desde los $1.000',
          cantidad: 'Por Kg'
        }
      ]
    }
  },
  methods: {
    enrutarProducto(entrada){
      return `/products/${entrada}`
    }
  }
}
</script>