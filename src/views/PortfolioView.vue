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
          description:
            "Création de l'application web Vinoways Territoire. Une application de découverte de l'univers viticole par région.",
          img: "vinoways.png",
          tags: ["HTML/CSS", "Apostrophe CMS", "VueJs", "Javascript"],
          link: "",
        },
        {
          title: "Road X",
          date: "Janvier, 2022",
          description:
            "Réalisation d'un mini-jeu spour la GameJam 2022, sur le thème de la dualité.",
          img: "roadx.jpg",
          tags: ["HTML/CSS", "Javascript"],
          link: "https://play.roadx.fun/",
        },
        {
          title: "ShotX",
          date: "Février, 2022",
          description:
            "Réalisation d'une application mobile, pour s'amuser entre amis en soirée.",
          img: "shotx.png",
          tags: ["Wordpress", "React Native", "Javascript"],
          link: "https://www.shotx.fr/",
        },
        {
          title: "Intégration Web",
          date: "Avril, 2021",
          description:
            "Intégration de la nouvelle charte graphique de l'entreprise Uccello Io.",
          img: "uccello.png",
          tags: ["HTML/CSS", "Tailwind CSS", "AlpineJs"],
          link: "https://github.com/uccellolabs/uccello/tree/3.x-lr",
        },
        {
          title: "Site vitrine",
          date: "Juillet, 2021",
          description:
            "Réalisation d'un site vitrine pour un gîte de location saisonnière.",
          img: "gite.png",
          tags: ["HTML/CSS", "Tailwind CSS"],
          link: "https://gitelespittos.fr/",
        },
        {
          title: "Covid-Tracker",
          date: "Mars, 2021",
          description:
            "Réalisation d'un tracker par pays pour les données du Covid-19.",
          img: "covidtracker.png",
          tags: ["HTML/CSS", "Tailwind CSS", "VueJs"],
          link: "/covid-tracker",
        },
      ],
    };
  },
  components: {
    PortfolioItem,
  },
};
</script>
