<template>
    <section id="products">
        <div class="products-container">
            <div class="product-block" v-for="product in products">
                <div class="product-image">
                    <img :src="loadImage(product.url)" :alt="product.name">
                </div>
                <div class="product-item-info">
                    <h2>{{product.amount}} л | {{product.power}} кВт | {{product.heating}}</h2>
                    <p>{{product.country}}</p>
                    <h1>{{product.name}}</h1>
                    <h3>{{product.price}} {{product.currency}}</h3>
                </div>
            </div>
        </div>
    </section>
</template>


<script>
  export default {
    name: 'ProductList',
    data () {
      return {}
    },
    props: ['products'],
    methods: {
      loadImage (path) {
        return require('./../../assets/images/boilers/'+path)
      }
    },
    watch: {}

  }
</script>
