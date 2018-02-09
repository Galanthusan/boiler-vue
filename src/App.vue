<template>
    <div id="app">
        <header-component/>
        <product-container-component/>
        <question-form-component/>
        <footer-component/>
    </div>
</template>


<script>
  import HeaderComponent from './components/HeaderComponent'
  import ProductContainerComponent from './components/products/ProductContainerComponent'
  import QuestionFormComponent from './components/QuestionFormComponent'
  import FooterComponent from './components/FooterComponent'

  export default {
    name: 'App',
    components: {
      HeaderComponent,
      ProductContainerComponent,
      QuestionFormComponent,
      FooterComponent
    }
  }
</script>
