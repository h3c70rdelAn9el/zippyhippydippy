<template>
  <div>
    <b-carousel
      id="carousel"
      v-model="slide"
      fade
      :interval="4000"
      controls
      indicators
      background="#ababab"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <div v-for="image in images" :key="image.id">
        <b-carousel-slide
          :caption="image.caption"
          :text="image.text"
          :img-src="image.src"
          class="carousel-item"
        >
          <p>
            {{ image.content }}
          </p>
        </b-carousel-slide>
      </div>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      slide: 0,
      sliding: null,
      images: [
        {
          caption: 'First slide',
          text: 'Nulla vitae elit libero, a pharetra augue mollis interdum.',
          src: require('../assets/img/henrik-donnestad-t2Sai-AqIpI-unsplash.jpg'),
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.'
        },
        {
          caption: 'Second slide',
          text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Earum, incidunt.',
          src: require('../assets/img/steve-johnson-e5LdlAMpkEw-unsplash.jpg')
        },
        {
          caption: 'Third slide',
          text: 'Qui nihil quaerat itaque sunt ex error minima dolorem distinctio velit',
          src: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          content: 'Quibusdam culpa, voluptatibus deserunt molestiae earum similique odit magnam.Cum, quam perferendis. Necessitatibus similique praesentium sapiente molestiae!'
        }
      ]
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style>
  #carousel {
    height: 100vh;
  }

  .carousel-item {
    height: 100vh;
  }

  .carousel-item img {
    height: 100%;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
  }

  .carousel-caption {
    font-family: 'Poppins', sans-serif;
    position: absolute;
    top: 35%;
  }

  .carousel-caption h3 {
    font-family: 'Abril Fatface', cursive;
    font-size: 45px;
  }
</style>
