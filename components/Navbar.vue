<template>
  <div class="sticky-top">
    <div class="row align-content-start justify-content-between">
      <b-button v-b-toggle.sidebar-variant class="menu-button ml-2 col-1 overflow-hidden">
        <b-icon icon="list" />
      </b-button>
      <div class="logo col-10 z-40 text-center">
        <nuxt-link to="/">
          <img src="../assets/img/LogoMakr-0oC9c0.png" alt="">
        </nuxt-link>
      </div>
      <div class="col-1" />
    </div>
    <b-sidebar id="sidebar-variant" title="" bg-variant="dark" text-variant="light" shadow>
      <div v-for="link in links" :key="link.id" class="px-3 py-2">
        <nuxt-link :to="link.route" class="link">
          {{ link.page }}
        </nuxt-link>
      </div>
    </b-sidebar>
  </div>
</template>

<script>
export default {
  data () {
    return {
      links: [
        {
          page: 'Home',
          route: '/'
        },
        {
          page: 'About',
          route: '/about'
        },
        {
          page: 'Projects',
          route: '/projects'
        },
        {
          page: 'Contact',
          route: '/contact'
        }
      ]
    }
  }
}
</script>

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

  .link {
    color: white;
  }

</style>
