<template>
    <section v-if="isSidebarOpen" id="product-sidebar">
        <div class="sidebar-block">

            <div class="filter-group">
                <h2>Тип нагрева</h2>
                <div class="input-list">
                    <div class="form-group" v-for="heating_type in filterData.heater_types">
                        <label> <input type="checkbox" v-bind:name="heating_type.name" :value="heating_type.name"
                                       v-model="heating_type.checked">{{heating_type.name}}</label>
                    </div>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Производитель</h2>
            <div class="input-list">
                <div class="form-group" v-for="brand in filterData.brands">
                    <label> <input type="checkbox" v-bind:name="brand.name" :value="brand.value"
                                   v-model="brand.checked">{{brand.name}}</label>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Объем, л</h2>
            <div class="input-list">
                <div class="form-group" v-for="amount in filterData.amounts">
                    <label><input type="checkbox" name="amount" v-bind:value="amount.value" v-model="amount.checked">{{amount.name}}</label>
                </div>
            </div>
        </div>

    </section>
</template>


<script>
  export default {
    data () {
      return {
        filterData: {
          heater_types: [
            {name: 'открытый ТЭН', checked: false},
            {name: 'закрытый ТЭН', checked: false}
          ],
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
        },
        isSidebarOpen : false
      }
    },
    methods: {
      toggle() {
        if(this.isSidebarOpen) {
          return this.hide();
        }
        else {
          this.show();
        }
      },
      
      hide () {
        //
        this.isSidebarOpen = false;
      },
      show () {
        //
        this.isSidebarOpen = true;
      }
    },
    watch: {
      filterData: {
        handler: function (value) { // watch it
          this.$parent.filterDataUpdate(value)
        },
        deep: 1
      },
    }
  }
</script>

