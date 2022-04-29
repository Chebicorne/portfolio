<template>
  <div class="portfolio">
    <section class="pt-20 px-8 lg:pt-[120px] pb-10 lg:pb-20">
      <div class="text-center text-white text-4xl font-bold mb-12">
        Mes créations
      </div>
      <div class="container mx-auto">
        <div class="flex flex-wrap -mx-4">
          <PortfolioItem
            v-for="item in portfolio"
            :key="item.id"
            :item="item"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import PortfolioItem from "@/components/PortfolioItem.vue";
export default {
  data() {
    return {
      portfolio: [
        {
          title: "VinoWays Territoire",
          date: "Avril, 2022",
          description: "Création de l'app web vinoWays Territoire",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["HTML/CSS", "Apostrophe CMS", "VueJs", "Javascript"],
          link: "",
        },
        {
          title: "Road X",
          date: "Janvier, 2022",
          description:
            "Réalisation d'un mini-jeu sur le thème de la dualité pour la GameJam 2022.",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["HTML/CSS", "Javascript"],
          link: "",
        },
        {
          title: "ShotX",
          date: "Février, 2022",
          description:
            "Réalisation d'une application mobile pour s'amuser entre amis en soirée.",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["Wordpress", "React Native", "Javascript"],
          link: "",
        },
        {
          title: "Intégration Web",
          date: "Avril, 2021",
          description:
            "Intégration de la nouvelle charte graphique de l'entreprise Uccello Io.",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["HTML/CSS", "AlpineJs"],
          link: "",
        },
        {
          title: "Site vitrine",
          date: "Juillet, 2021",
          description:
            "Réalisation d'un site vitrine pour un gîte de location saisonnière.",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["HTML/CSS"],
          link: "",
        },
        {
          title: "Covid-Tracker",
          date: "Mars, 2021",
          description: "Réalisation d'un tracker pour les données du Covid-19.",
          img: "https://cdn.tailgrids.com/1.0/assets/images/cards/card-01/image-01.jpg",
          tags: ["HTML/CSS", "VueJs"],
          link: "",
        },
      ],
    };
  },
  components: {
    PortfolioItem,
  },
};
</script>
