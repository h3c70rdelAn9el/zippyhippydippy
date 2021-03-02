<template>
  <div class="sticky-top">
    <div class="row align-content-start justify-content-between">
      <b-button v-b-toggle.sidebar-variant class="menu-button col-1 overflow-hidden">
        <b-icon icon="list" />
      </b-button>
      <div class="logo col-10 text-center">
        <img src="../assets/img/LogoMakr-0nO1Fe.png" alt="">
      </div>
      <div class="col-1" />
    </div>
    <b-sidebar id="sidebar-variant" title="" bg-variant="dark" text-variant="light" shadow>
      <div class="px-3 py-2">
        <nuxt-link to="/about">
          <p>About</p>
        </nuxt-link>
      </div>
    </b-sidebar>
  </div>
</template>

<style scoped>
  .logo {
  }

  .logo img {
    border-radius: 30px;
  }

  .menu-button {
    height: 40px;
  }
</style>
