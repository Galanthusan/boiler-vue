<template>
    <div>
        <sub-navigation-component/>
        <products-list-component :products="filteredProducts"/>
        <product-sidebar-component  ref="productSidebarComponent"/>
    </div>
</template>

<script>
  import SubNavigationComponent from './../../components/products/SubNavigationComponent'
  import ProductsListComponent from './../../components/products/ProductsListComponent'
  import ProductSidebarComponent from './../../components/products/ProductSidebarComponent'

  export default {
    name: 'ProductContainerComponent',
    components: {
      SubNavigationComponent,
      ProductsListComponent,
      ProductSidebarComponent,
    },
    data () {
      return {
        products: [
          {
            name: 'WILLER EV100DR fine',
            brand_name: 'willer',
            url: '1.png',
            amount: 100,
            amount_name: '100 - 149',
            power: 2.0,
            heating: 'закрытый ТЭН',
            heater_type_internal: true,
            heater_type_external: false,
            country: 'Китай',
            price: 6032,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS PRO R 65V SLIM',
            brand_name: 'ariston',
            url: '2.png',
            amount: 65,
            amount_name: '50 - 79',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Россия',
            price: 3633,
            currency: 'грн'
          },
          {
            name: 'ELECTROLUX EWH 30 AXIOmatic Slim',
            brand_name: 'electrolux',
            url: '3.png',
            amount: 30,
            amount_name: '30 - 49',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Китай',
            price: 2600,
            currency: 'грн'
          },
          {
            name: 'ZANUSSI ZWH/S 100 Smalto',
            brand_name: 'zanussi',
            url: '4.png',
            amount: 100,
            amount_name: '100 - 149',
            power: 2.0,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Китай',
            price: 4300,
            currency: 'грн'
          },
          {
            name: 'BOSCH Tronic 2000 T 50B',
            brand_name: 'bosch',
            url: '5.png',
            amount: 50,
            amount_name: '50 - 79',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Германия',
            price: 2999,
            currency: 'грн'
          },
          {
            name: 'RODA Palladium 50',
            brand_name: 'roda',
            url: '6.png',
            amount: 50,
            amount_name: '50 - 79',
            power: 1.6,
            heating: 'закрытый ТЭН',
            heater_type_internal: true,
            heater_type_external: false,
            country: 'Болгария',
            price: 5299,
            currency: 'грн'
          },
          {
            name: 'RODA Aqua INOX 80 VM',
            brand_name: 'roda',
            url: '7.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 2.0,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Китай',
            price: 5699,
            currency: 'грн'
          },
          {
            name: 'ATLANTIC CLASSIC VM 80 N4L',
            brand_name: 'atlantic',
            url: '8.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Украина',
            price: 1976,
            currency: 'грн'
          },
          {
            name: 'GORENJE OGBS 80 SMV9',
            brand_name: 'gorenje',
            url: '9.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 2.0,
            heating: 'закрытый ТЭН',
            heater_type_internal: true,
            heater_type_external: false,
            country: 'Сербия',
            price: 7002,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30 D',
            brand_name: 'ariston',
            url: '10.png',
            amount: 30,
            amount_name: '30 - 49',
            power: 2.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Россия',
            price: 5115,
            currency: 'грн'
          },
          {
            name: 'ELECTROLUX EWH 80 Royal Flash',
            brand_name: 'electrolux',
            url: '11.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 2.0,
            heating: 'закрытый ТЭН',
            heater_type_internal: true,
            heater_type_external: false,
            country: 'Китай',
            price: 7277,
            currency: 'грн'
          },
          {
            name: 'ELECTROLUX EWH 50 AXIOmatic Slim',
            brand_name: 'electrolux',
            url: '12.png',
            amount: 50,
            amount_name: '50 - 79',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Китай',
            price: 2920,
            currency: 'грн'
          },
          {
            name: 'BOSCH Tronic 2000 T 30SB',
            brand_name: 'bosch',
            url: '13.png',
            amount: 30,
            amount_name: '30 - 49',
            power: 1.2,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Болгария',
            price: 2899,
            currency: 'грн'
          },
          {
            name: 'GORENJE GBK 80 LN',
            brand_name: 'gorenje',
            url: '14.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 2.0,
            heating: 'закрытый ТЭН',
            heater_type_internal: true,
            heater_type_external: false,
            country: 'Сербия',
            price: 7772,
            currency: 'грн'
          },
          {
            name: 'GORENJE TGR 80 NGV9',
            brand_name: 'gorenje',
            url: '15.png',
            amount: 80,
            amount_name: '80 - 99',
            power: 2.0,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Сербия',
            price: 4020,
            currency: 'грн'
          },
          {
            name: 'ARISTON ABS VLS EVO PW 30',
            brand_name: 'ariston',
            url: '16.png',
            amount: 30,
            amount_name: '30 - 49',
            power: 1.5,
            heating: 'открытый ТЭН',
            heater_type_internal: false,
            heater_type_external: true,
            country: 'Россия',
            price: 5115,
            currency: 'грн'
          },
        ],
        filterData: {
          heater_types : [
            {name: 'открытый ТЭН', checked: false},
            {name: 'закрытый ТЭН', checked: false}
          ],
          heater_type_external: '',
          heater_type_internal: '',
          brands: [
            {name: 'Ariston', value: 'ariston', checked: false},
            {name: 'Atlantic', value: 'atlantic', checked: false},
            {name: 'Bosch', value: 'bosch', checked: false},
            {name: 'Electrolux', value: 'electrolux', checked: false},
            {name: 'Gorenje', value: 'gorenje', checked: false},
            {name: 'Roda', value: 'roda', checked: false},
            {name: 'Willer', value: 'willer', checked: false},
            {name: 'Zanussi', value: 'zanussi', checked: false},
          ],
          amounts: [
            {name: 'менее 30', value: '30l', checked: false},
            {name: '30 - 49', value: '30-49l', checked: false},
            {name: '50 - 79', value: '50-79l', checked: false},
            {name: '80 - 99', value: '80-99l', checked: false},
            {name: '100 - 149', value: '100-149l', checked: false},
            {name: '150 - 199', value: '150-199l', checked: false},
            {name: 'свыше 200', value: '200l', checked: false},
          ]
        }
      }
    },
    methods: {
      filterDataUpdate (filterData) {
        console.log(filterData)
        this.filterData = filterData
      },
      sidebarToggle() {
        this.$refs.productSidebarComponent.toggle();
      }
    },
    computed: {
      filteredProducts: function () {
        let $component = this

        return this.products.filter(function (product) {
          let isHeaterFiltered = false;
          let isBrandFiltered = false;
          let isAmountFiltered = false;
          

          let checkedHeaters = $component.filterData.heater_types.filter(function (heater) {
            return heater.checked
          })  
          
          if (checkedHeaters.length) {
            checkedHeaters.forEach(function (heater) {
              if (product.heating === heater.name) {
                isHeaterFiltered = true
              }
            })
          }
          else {
            isHeaterFiltered = true
          }
          
          let checkedBrands = $component.filterData.brands.filter(function (brand) {
            return brand.checked
          })

          if (checkedBrands.length) {
            checkedBrands.forEach(function (brand) {
              if (product.brand_name === brand.value) {
                isBrandFiltered = true
              }
            })
          }
          else {
            isBrandFiltered = true
          }

          let checkedAmounts = $component.filterData.amounts.filter(function (amount) {
            return amount.checked
          });
          
          if (checkedAmounts.length) {
            checkedAmounts.forEach(function (amount) {
              if (product.amount_name === amount.name) {
                isAmountFiltered = true
              }
            })
          }
          else {
            isAmountFiltered = true;
          }
  

          if (isHeaterFiltered && isBrandFiltered && isAmountFiltered && true) {
            console.log(isHeaterFiltered + ' ' + isBrandFiltered + ' ' + isAmountFiltered)
            return true
          }
          else {
            return false
          }

        })
      }
    }

  }
</script>
