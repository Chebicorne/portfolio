<template>
  <div class="flex flex-col items-center">
    <!-- Box 1 -->
    <div class="w-full lg:w-1/2 bg-white bg-opacity-70 p-8 text-center rounded">
      <h3 class="text-3xl text-orange-500 font-bold mb-4">Cas</h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">Nouveau :</span>
        {{ numberWithCommas(stats.NewConfirmed) }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">Total :</span>
        {{ numberWithCommas(stats.TotalConfirmed) }}
      </div>
    </div>

    <!-- Box 2 -->
    <div
      class="w-full md:w-1/2 bg-white bg-opacity-70 p-8 text-center rounded mt-12"
    >
      <h3 class="text-3xl text-red-900 font-bold mb-4">Morts</h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">Nouveau :</span>
        {{ numberWithCommas(stats.NewDeaths) }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">Total :</span>
        {{ numberWithCommas(stats.TotalDeaths) }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DataBoxes",
  props: ["stats"],
  methods: {
    numberWithCommas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
  },
};
</script>
