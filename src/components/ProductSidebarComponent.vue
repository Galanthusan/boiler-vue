<template>
    <section id="product-sidebar">
        <div class="sidebar-block">

            <div class="filter-group">
                <h2>Тип нагрева</h2>
                <div class="input-list">
                    <div class="form-group">
                        <label><input type="checkbox" name="heater_type" value="external" id="heater_type_external">Открытый ТЭН</label>
                    </div>
                    <div class="form-group">
                        <label><input type="checkbox" name="heater_type" value="internal" id="heater_type_internal">Закрытый ТЭН</label>
                    </div>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Производитель</h2>
            <div class="input-list">
                <div class="form-group">
                    <label> <input type="checkbox" name="brand" value="ariston" id="brand-ariston">Ariston</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="atlantic" id="brand-atlantic">Atlantic</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="bosch" id="brand-bosch">Bosch</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="electrolux" id="brand-electrolux">Electrolux</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="gorenje" id="brand-gorenje">Gorenje</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox"name="brand" value="roda" id="brand-roda">Roda</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="willer" id="brand-willer">Willer</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="brand" value="zanussi" id="brand-zanussi">Zanussi</label>
                </div>
            </div>
        </div>

        <div class="filter-group">
            <h2>Объем, л</h2>
            <div class="input-list">
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="30l" id="amount-30">менее 30</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="30-49l" id="amount-30-49">30 - 49</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="50-79l" id="amount-50-79">50 - 79</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="80-99l" id="amount-80-99">80 - 99</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="100-149l" id="amount-100-149">100 - 149</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="150-199l" id="amount-150-199">150 - 199</label>
                </div>
                <div class="form-group">
                    <label><input type="checkbox" name="amount" value="200l" id="amount-200">свыше 200</label>
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
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>
