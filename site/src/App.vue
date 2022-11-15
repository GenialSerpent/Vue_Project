<template>
  <div>
    <GamesList v-bind:listLeft="listLeft" v-bind:listRight="listRight" />
  </div>
</template>

<script>
import GamesList from "./components/GamesList";
import { mapGetters } from "vuex";
export default {
  name: "App",
  data() {
    return {
      listLeft: [
        {
          id: 1,
          imgSrc:
            "https://n9e5v4d8.ssl.hwcdn.net/uploads/thumbnails/64957c8ae8067f73e00186e477de7bb2_1600x900.png",
          title: "WARFRAME",
          completed: false,
        },
        {
          id: 2,
          imgSrc:
            "https://static-assets-prod.epicgames.com/competitive/static/webpack/1d89ee10c18f54afa33cf8063c27d7d4.jpg",
          title: "FORTNITE",
          completed: false,
        },
        {
          id: 3,
          imgSrc:
            "https://fs-prod-cdn.nintendo-europe.com/media/images/10_share_images/games_15/nintendo_switch_4/2x1_NSwitch_Omori_image1600w.jpg",
          title: "OMORI",
          completed: false,
        },
      ],
      listRight: [
        {
          id: 1,
          imgSrc:
            "https://cdn1.epicgames.com/salesEvent/salesEvent/EGS_GenshinImpact_miHoYoLimited_S2_1200x1600-c12cdcc2cac330df2185aa58c508e820",
          title: "GENSHIN IMPACT",
          completed: false,
        },
        {
          id: 2,
          imgSrc:
            "https://play-lh.googleusercontent.com/JRd05pyBH41qjgsJuWduRJpDeZG0Hnb0yjf2nWqO7VaGKL10-G5UIygxED-WNOc3pg",
          title: "PUBG",
          completed: false,
        },
        {
          id: 3,
          imgSrc:
            "http://pm1.narvii.com/6782/033bc5cad1c5b24ee1b44cb553820fece97b484av2_00.jpg",
          title: "HELLO CHARLOTTE",
          completed: false,
        },
      ],
    };
  },
  components: {
    GamesList,
  },
  computed: {
    ...mapGetters(["getCount"]),
  },
};
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
