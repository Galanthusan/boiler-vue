<template>
    <section id="products">
        <div class="products-container">
            <div class="product-block" v-for="product in products">
                <div class="product-image">
                    <img src="./../assets/images/boilers/1.png" :alt="product.name">
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
    name: 'HelloWorld',
    data () {
      return {
        products: [
          {
          name: 'ARISTON ABS VLS EVO PW 30 ',
          url: './../assets/images/boilers/1.png',
          amount: 30,
          power: 1.5,
          heating: 'открытый ТЭН',
          country: 'Россия',
          price: 5332,
          currency: 'грн'
        },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 ',
            url: './../assets/images/boilers/1.png',
            amount: 30,
            power: 1.5,
            heating: 'открытый ТЭН',
            country: 'Россия',
            price: 5332,
            currency: 'грн'
          },
        ]
      }
    }
  }
</script>
