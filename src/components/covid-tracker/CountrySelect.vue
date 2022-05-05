<template>
  <select
    @change="onChange"
    v-model="selected"
    class="form-select w-full lg:w-1/2 mt-10 block m-4 border p-3 rounded mx-auto"
  >
    <option value="0">Monde</option>
    <option v-for="country in countries" :value="country.ID" :key="country.id">
      {{ country.Country }}
    </option>
  </select>
</template>

<script>
export default {
  name: "CountrySelect",
  props: ["countries"],
  data() {
    return {
      selected: 0,
    };
  },
  methods: {
    onChange() {
      const country = this.countries.find(
        (country) => country.ID === this.selected
      );
      this.$emit("get-country", country);
    },
  },
};
</script>
