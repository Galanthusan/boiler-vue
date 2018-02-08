<template>
    <section id="question-form">
        <div class="left-side-section">
            <h2>Задать вопрос</h2>
            <div class="input-name">
                <input type="text" placeholder="Ваше имя">
            </div>
            <div class="input-email">
                <input type="text" placeholder="Ваш e-mail">
            </div>
            <div class="input-phone-number">
                <input type="text" placeholder="Ваш телефон">
            </div>
            <textarea placeholder="Ваш вопрос"></textarea>
            <div class="question-form-button">
                <button>Отправить</button>
            </div>
        </div>
        <div class="right-side-section">
            <div class="right-side-item-image">
                <img src="./../assets/images/bubbles.png" alt="">
            </div>
        </div>
    </section>
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
