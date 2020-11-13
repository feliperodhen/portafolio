<template>
  <i-navbar class="_background-transparent">
    <i-navbar-brand :to="{ name: 'index' }"
      >
    <img v-show="isDark" class="logo" src="~/assets/felipe-rodriguez-logo-white.svg" alt=""
    />
        <img v-show="!isDark" class="logo" src="~/assets/felipe-rodriguez-logo.svg" alt=""
    />
    </i-navbar-brand>

    <div class="logo-point">
      <svg
        version="1.1"
        id="Capa_2_1_"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        x="0px"
        y="0px"
        viewBox="0 0 260 260"
        style="enable-background: new 0 0 260 260"
        xml:space="preserve"
      >
        <path fill="#F89808">
          <animate
            attributeName="d"
            dur="1440ms"
            repeatCount="indefinite"
            keyTimes="0;
                       .0625;
                       .208333333;
                       .3125;
                       .395833333;
                       .645833333;
                       .833333333;
                       1"
            calcMode="spline"
            keySplines="0,0,1,1;
                         .42,0,.58,1;
                         .42,0,1,1;
                         0,0,.58,1;
                         .42,0,.58,1;
                         .42,0,.58,1;
                         .42,0,.58,1"
            values="M 0,0 
                     C 50,0 50,0 100,0
                     100,50 100,50 100,100
                     50,100 50,100 0,100
                     0,50 0,50 0,0
                     Z;

                     M 0,0 
                     C 50,0 50,0 100,0
                     100,50 100,50 100,100
                     50,100 50,100 0,100
                     0,50 0,50 0,0
                     Z;

                     M 50,0 
                     C 75,25 75,25 100,50 
                     75,75 75,75 50,100
                     25,75 25,75 0,50
                     25,25 25,25 50,0
                     Z;

                     M 25,50 
                     C 37.5,25 37.5,25 50,0 
                     75,50 75,50 100,100
                     50,100 50,100 0,100
                     12.5,75 12.5,75 25,50
                     Z;

                     M 25,50 
                     C 37.5,25 37.5,25 50,0 
                     75,50 75,50 100,100
                     50,100 50,100 0,100
                     12.5,75 12.5,75 25,50
                     Z;

                     M 50,0
                     C 77.6,0 100,22.4 100,50 
                     100,77.6 77.6,100 50,100
                     22.4,100, 0,77.6, 0,50
                     0,22.4, 22.4,0, 50,0
                     Z;
                     
                     M 50,0
                     C 77.6,0 100,22.4 100,50 
                     100,77.6 77.6,100 50,100
                     22.4,100, 0,77.6, 0,50
                     0,22.4, 22.4,0, 50,0
                     Z;
                     
                     M 100,0 
                     C 100,50 100,50 100,100
                     50,100 50,100 0,100
                     0,50 0,50 0,0
                     50,0 50,0 100,0
                     Z;"
          />
        </path>
      </svg>
    </div>
    <i-navbar-items>
      <i-nav> </i-nav>
      <i-nav>
        <i-nav-item href="#inicio" v-show="!isDark">Inicio</i-nav-item>
        <i-nav-item href="#inicio" v-show="!isDark"
          >Habilidades</i-nav-item
        >
        <i-nav-item href="#inicio" v-show="!isDark"
          >Trabajos</i-nav-item
        >
        <i-nav-item href="#inicio" v-show="!isDark"
          >Contacto</i-nav-item
        >
        <i-nav-item href="#inicio" v-show="isDark">Home</i-nav-item>
        <i-nav-item href="#inicio" v-show="isDark">Skills</i-nav-item>
        <i-nav-item href="#inicio" v-show="isDark">Works</i-nav-item>
        <i-nav-item href="#inicio" v-show="isDark">Contact</i-nav-item>
        <i-button
          @click="
            toggleDarkMode();
            toggleDark();
          "
        >
          <i-icon icon="light" />
        </i-button>
      </i-nav>
    </i-navbar-items>
  </i-navbar>
</template>

<script>
export default {
  name: "PageNav",
  data() {
    return {
      isDark: false,
    };
  },
  methods: {
    toggleDarkMode() {
      this.$inkline.config.variant =
        this.$inkline.config.variant === "light" ? "dark" : "light";
    },
    toggleDark() {
      this.isDark = !this.isDark;
    },
  },
};
</script>

<style scoped>
.logo {
  width: 60px;
}

.logo-point {
  width: 25px;
  top: 52px;
  left: 55px;

  position: absolute;
}
</style>


