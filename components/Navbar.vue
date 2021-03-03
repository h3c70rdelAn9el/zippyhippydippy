
<template>
  <div class="sticky-top z-20">
    <div class="row align-content-start justify-content-between">
      <b-button v-b-toggle.sidebar-variant class="menu-button ml-2 col-1 overflow-hidden">
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
    margin-left: -10px;
  }

  .logo img {
    border-radius: 30px;
    width: 150px;
  }

  .menu-button {
    height: 40px;
  }
</style>

<!--
<template>
  <b-navbar class="navbar row" toggleable="md" type="light">
    <b-navbar-brand href="#" class="brand col">
      brand
    </b-navbar-brand>

    <b-navbar-toggle target="navbar-toggle-collapse">
      <template v-slot:default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up" class="nav-icon" />
        <b-icon v-else icon="chevron-bar-down" class="nav-icon" />
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav v-for="link in links" :key="link.id" class="nav-links ml-auto">
        <b-nav-item v-scroll-to="link.route" href="#" class="">
          {{ link.name }}
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  data () {
    return {
      links: [
        {
          name: 'Home',
          route: '#'
        },
        {
          name: 'About',
          route: '#about-section'
        },
        {
          name: 'Team',
          route: '#team-section'
        },
        {
          name: 'Contact',
          route: '#contact'
        }
      ]
    }
  }
}
</script>

<style scoped>
  /* .navbar {
    background: rgb(111, 45, 155);
    width: 100%;
  }
  .nav-icon {
    color: rgb(233, 38, 240);
  }

 .navbar a:hover {
    background-color: rgb(163, 133, 184);
    border-radius: 5px;
  }

  .navbar a {
    padding-left: 2px;
  } */
</style>
-->
