<template>

  <div class="relative bg-gradient-to-r from-green-400 to-blue-500 md:pt-32 pb-32 pt-12 w-full">
    <div class="px-4 md:px-10 mx-auto w-full">
      <div>
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <h2 class="text-2xl font-bold mb-2 text-gray-800">RothC example simulation configuration</h2>
          <p class="text-gray-700">Input the custom values in the fields below. Default values as placeholder text will be used if none provided.</p>
        </div>
        <div class="flex flex-wrap mt-10">

        <Rothctemplate
        configParamtype="rainfall"
        />

        <Rothctemplate
        configParamtype="openPanEvap"
        />

        <Rothctemplate
        configParamtype="avgAirTemp"
        />

        <Rothctemplate
        configParamtype="presCM"
        />

        <Rothctemplate
        configParamtype="soilCover"
        />

        <Rothctemplate
        configParamtype="initSoil"
        />

        <Rothctemplate
        configParamtype="soil"
        />

        </div>

      </div>
    </div>
</div>

</template>

<script>
import Rothctemplate from "@/views/flint/Rothctemplate.vue"

export default {

  components: {
    Rothctemplate,
  },
}
</script>
