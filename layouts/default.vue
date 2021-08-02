<template xmlns="http://www.w3.org/1999/html">
  <v-app light>
    <v-main>
      <v-container fluid>
        <MainNavbar />
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      rules: [
        value => !!value || 'Required.',
        value => (value && value.length >= 3) || 'Min 3 characters',
      ],
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: "Apercu";
  src: url("static/fonts/Apercu-Font/Apercu Medium.otf");
}
@font-face {
  font-family: "Apercu-italic";
  src: url("static/fonts/Apercu-Font/Apercu Medium italic.otf");
}
*{
  font-family: "Apercu";
}
.v-application {
  background: crimson !important;
}
.main-navbar {
  height: 40px;
  background-color: rgba(0, 0, 0, 0.12);
  color: white;
}
.main-navbar-item:not(.not-background) {
  min-width: 32px;
  max-height: 32px;
  background-color: rgba(255, 255, 255, 0.22);
}
.input-search-navbar{
  min-width: 200px;
  height: 24px;
  cursor: pointer;
  span{
    cursor: pointer;
  }
}
.site-name-navbar{
  font-family: "Apercu-italic";
  font-size: 1.1rem;

}
.input-search-in-modal {
  width: 100%;
  margin-bottom: -10px;
  input{
    text-align: center;
  }
  input::placeholder{
    color: rgba(1, 94, 104, 0.53) !important;
  }
}
</style>
