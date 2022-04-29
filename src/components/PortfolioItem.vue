<template>
  <div class="w-full md:w-1/2 xl:w-1/4 px-4">
    <div class="bg-white rounded-lg overflow-hidden mb-10">
      <img :src="item.img" alt="image" class="w-full" />
      <div class="p-8 sm:p-9 md:p-7 xl:p-9 text-center">
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
