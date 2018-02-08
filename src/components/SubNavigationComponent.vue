<template>
    <section id="sub-navigation">
        <div class="filter-icon" id="filter-button"></div>

        <div class="filter-icon-label" id="filter-text">Скрыть фильтры</div>

        <div class="sub-navigation-item-input">
            <select id="product-parameters">
                <option value="" disabled selected hidden>Сортировать по</option>
                <option class="selected-item-input">Цена: ниже - выше</option>
                <option class="selected-item-input">Цена: выше - ниже</option>
                <option class="selected-item-input">A-Z</option>
            </select>
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
