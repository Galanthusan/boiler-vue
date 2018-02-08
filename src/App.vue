<template>
  <div id="app">
   <header-component/>
   <sub-navigation-component/>
   <products-component/>
   <product-sidebar-component/>
   <question-form-component/>
   <footer-component/>
      
  </div>
</template>


<script>

import HeaderComponent from './components/HeaderComponent'
import SubNavigationComponent from './components/SubNavigationComponent'
import ProductsComponent from './components/ProductsComponent'
import ProductSidebarComponent from './components/ProductSidebarComponent'
import QuestionFormComponent from './components/QuestionFormComponent'
import FooterComponent from './components/FooterComponent'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    SubNavigationComponent,
    ProductsComponent,
    ProductSidebarComponent,
    QuestionFormComponent,
    FooterComponent
  }
}
</script>
