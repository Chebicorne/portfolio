<template>
  <main v-if="!loading">
    <DataTitle />
    <DataBoxes :stats="stats" />
    <CountrySelect @get-country="getCountryData" :countries="countries" />
    <button
      v-if="stats.Country"
      @click="clearCountryData"
      class="flex justify-center bg-green-700 text-white rounded p-3 mt-10 w-full md:w-1/2 mx-auto focus:outline-none hover:bg-green-600"
    >
      Reset
    </button>
  </main>
</template>

<script>
import DataTitle from "../components/covid-tracker/DataTitle";
import DataBoxes from "../components/covid-tracker/DataBoxes";
import CountrySelect from "../components/covid-tracker/CountrySelect";
export default {
  name: "CovidView",
  components: {
    DataTitle,
    DataBoxes,
    CountrySelect,
  },
  data() {
    return {
      loading: true,
      title: "Global",
      dataDate: "",
      stats: {},
      countries: [],
    };
  },
  methods: {
    async fetchCovidData() {
      const res = await fetch("https://api.covid19api.com/summary");
      return res.json();
    },
    getCountryData(country) {
      this.stats = country;
      this.title = country.Country;
    },
    async clearCountryData() {
      this.loading = true;
      const data = await this.fetchCovidData();
      this.title = "Global";
      this.stats = data.Global;
      this.loading = false;
    },
  },
  async created() {
    const data = await this.fetchCovidData();
    this.dataDate = data.Date;
    this.stats = data.Global;
    this.countries = data.Countries;
    this.loading = false;
  },
};
</script>
