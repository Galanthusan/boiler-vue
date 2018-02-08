<template>
    <section id="product-sidebar">
        <div class="sidebar-block">

            <div class="filter-group">
                <h2>Тип нагрева</h2>
                <div class="input-list">
                    <div class="form-group">
                        <label><input type="checkbox" name="heater_type_external" value="true" id="heater_type_external" v-model="filterData.heater_type_external">Открытый ТЭН</label>
                    </div>
                    <div class="form-group">
                        <label><input type="checkbox" name="heater_type_internal" value="true" id="heater_type_internal" v-model="filterData.heater_type_internal">Закрытый ТЭН</label>
                    </div>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Производитель</h2>
            <div class="input-list">
                <div class="form-group" v-for="brand in filterData.brands">
                    <label> <input type="checkbox" v-bind:name="brand.name" :value="brand.value" id="brand-ariston" v-model="brand.checked">{{brand.name}}</label>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Объем, л</h2>
            <div class="input-list">
                <div class="form-group" v-for="amount in filterData.amounts">
                    <label><input type="checkbox" name="amount" v-bind:value="amount.value" id="amount-30" v-model="amount.checked">{{amount.name}}</label>
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
           heater_type_external: '',
           heater_type_internal: '',
           brands:  [
             { name : 'Ariston', value: 'ariston', checked: false },
             { name : 'Atlantic', value: 'atlantic', checked: false },
             { name : 'Bosch', value: 'bosch', checked: false },
             { name : 'Electrolux', value: 'electrolux', checked: false },
             { name : 'Gorenje', value: 'gorenje', checked: false },
             { name : 'Roda', value: 'roda', checked: false },
             { name : 'Willer', value: 'willer', checked: false },
             { name : 'Zanussi', value: 'zanussi', checked: false },
           ],
           amounts: [
             { name : 'менее 30', value: '30l', checked: false },
             { name : '30 - 49', value: '30-49l', checked: false },
             { name : '50 - 79', value: '50-79l', checked: false },
             { name : '80 - 99', value: '80-99l', checked: false },
             { name : '100 - 149', value: '100-149l', checked: false },
             { name : '150 - 199', value: '150-199l', checked: false },
             { name : 'свыше 200', value: '200l', checked: false },
           ]
        },
      }
    },
    watch: {
      filterData: {
        handler: function (value) { // watch it
          console.log(value);
          // this.$parent.onFilterUpdate(value);
        },
        deep: 1
      },
    }
  }
</script>

