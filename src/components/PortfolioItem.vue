<template>
  <div class="w-full md:w-1/2 xl:w-1/3 px-4">
    <div class="bg-white rounded-lg overflow-hidden mb-10">
      <img
        :src="require(`@/assets/${item.img}`)"
        alt="image"
        class="w-full border-b border-gray-500"
      />
      <div class="w-full flex mt-2 flex-wrap">
        <div
          class="flex flex-nowrap px-4 py-1 rounded-full bg-black mx-2 my-1 uppercase font-bold text-sm text-white"
          v-for="tag in item.tags"
          :key="tag.id"
        >
          {{ tag }}
        </div>
      </div>
      <div class="p-5 sm:p-6 md:p-7 xl:p-5 text-center">
        <h3 class="flex justify-center items-center mb-6">
          <a
            href=""
            class="font-semibold text-dark text-xl sm:text-[22px] md:text-xl lg:text-[22px] xl:text-xl 2xl:text-[22px] block"
          >
            {{ item.title }}
          </a>
          <span class="ml-3 flex flex-nowrap">{{ item.date }}</span>
        </h3>
        <p class="text-base text-body-color leading-relaxed mb-7">
          {{ item.description }}
        </p>
        <a
          :href="item.link"
          target="_blank"
          class="inline-block py-2 px-7 border border-[#E5E7EB] rounded-full text-base text-body-color font-medium hover:border-primary hover:bg-purple-600 hover:text-white hover:cursor-pointer transition"
        >
          Découvrir
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PortfolioItem",
  props: {
    item: Object,
  },
};
</script>
