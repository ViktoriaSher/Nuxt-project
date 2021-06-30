<template>
  <div class="wrapper">
    <nav>
      <span class="logotype">Extremo</span>
      <div class="forNuxtLinks">
        <nuxt-link class="nuxtLink" exact active-class="activeLink" to="/"
          >Home</nuxt-link
        >
        <nuxt-link class="nuxtLink" active-class="activeLink" to="/top">
          Top rated</nuxt-link
        >
      </div>
    </nav>
    <div style="height:100%; padding-top:90px">
      <nuxt></nuxt>
    </div>
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class=" nav">
          <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-title>
      </v-card>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"]
    };
  }
};
</script>
<style lang="scss">
@font-face {
  font-family: "AlFresco";
  src: url("../assets/fonts/AlFresco.ttf");
}
@font-face {
  font-family: "EB Garamond", serif;
  src: url("../assets/fonts/EBGaramond-VariableFont_wght.ttf");
}
%toCenter {
  display: flex;
  justify-content: center;
  align-items: center;
}
nav {
  position: fixed;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 90px;
  background-color: #d6d1ca;
  box-sizing: border-box;

  box-shadow: 0px -6px 50px black;
  z-index: 1;
  .forNuxtLinks {
    @extend %toCenter;
    padding-right: 100px;
    .nuxtLink {
      position: relative;
      cursor: pointer;
      color: white;
      font-size: 32px;
      text-decoration: none;
      margin-left: 30px;
    }
  }
}

.activeLink {
  font-weight: bold;
  border-bottom: 3px solid white;
}
.logotype {
  font-family: "AlFresco";
  font-size: 69px;
  color: white;
  padding-left: 200px;
}
.wrapper {
  width: 100%;
  height: 100%;
}
.nav {
  display: flex;
  justify-content: center;
  background-color: #d6d1ca !important;
}
</style>
