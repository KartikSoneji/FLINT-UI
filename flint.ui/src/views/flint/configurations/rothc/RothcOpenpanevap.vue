<template>

  <div class="relative bg-gradient-to-r from-green-400 to-blue-500 md:pt-32 pb-32 pt-12 w-full">
    <div class="px-4 md:px-10 mx-auto w-full">
      <div>
      <div class="bg-white p-6 rounded-lg shadow-lg">
    <h2 class="text-2xl font-bold mb-2 text-gray-800">RothC example simulation configuration</h2>
    <p class="text-gray-700">Input the custom values in the fields below. Default values as placeholder text will be used if none provided.</p>
  </div>

<div class="flex flex-wrap mt-10"> 

  <div class="w-full px-4 content-center rounded-md m-12 mb-5">
        <h1 class="flex-auto text-xl font-semibold">
        openPanEvap - data_orig
        </h1>
    <textarea 
    class="form-textarea mt-1 block w-full" 
    rows="5" 
    placeholder="" 
    v-model="newconfig_openPanEvap_data_orig"
    >
    </textarea>
    
  </div>

  <div class="w-full px-4 content-center rounded-md m-12 mb-5">
        <h1 class="flex-auto text-xl font-semibold">
        openPanEvap - data_month_avg
        </h1>
    <textarea 
    class="form-textarea mt-1 block w-full" 
    rows="5" 
    placeholder="" 
    v-model="newconfig_openPanEvap_data_month_avg"
    >
    </textarea>
    
  </div>

  <div class="w-full px-4 content-center rounded-md m-12 mb-5">
        <h1 class="flex-auto text-xl font-semibold">
        openPanEvap - data_lastyearcopy
        </h1>
    <textarea 
    class="form-textarea mt-1 block w-full" 
    rows="5" placeholder="" 
    v-model="newconfig_openPanEvap_data_lastyearcopy"
    >
    </textarea>
    
  </div>



</div>

</div>
</div>
</div>

</template>

<script>

export default {
  computed: {
    newconfig_openPanEvap_data_orig: {
      get() {
         return this.$store.state.RothC_config.Variables[9].openPanEvap.transform.data_orig
      },
      set(newValue) {
        let tempval = newValue;
        this.$store.commit('setNewConfig_openPanEvap_data_orig', tempval)
      }
    },

    newconfig_openPanEvap_data_month_avg: {
      get() {
         return this.$store.state.RothC_config.Variables[9].openPanEvap.transform.data_month_avg
      },
      set(newValue) {
        let tempval = newValue;
        this.$store.commit('setNewConfig_openPanEvap_data_month_avg', tempval)
      }
    },

    newconfig_openPanEvap_data_lastyearcopy: {
      get() {
         return this.$store.state.RothC_config.Variables[9].openPanEvap.transform.data_lastyearcopy
      },
      set(newValue) {
        let tempval = newValue;
        this.$store.commit('setNewConfig_openPanEvap_data_lastyearcopy', tempval)
      }
    },
  },
}
</script>
