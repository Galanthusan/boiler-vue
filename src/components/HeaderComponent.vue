<template>
    <header id="header">

        <div class="container">
            <ul class="navigation">
                <li><a href="#" class="active">Бойлера</a></li>
                <li><a href="#">Аксессуары</a></li>
                <li><a href="#">Контакты</a></li>
            </ul>
            <div class="logo">
                <img src="./../assets/images/logo.png" alt="">
            </div>
            <div class="header-icons">
                <div class="search-icon"></div>
                <div class="basket-icon"></div>
            </div>
        </div>

    </header>
</template>



<script>
  export default {
    name: 'HelloWorld',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>
