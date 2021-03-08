<template>
  <div class="works">
    Works!
    <div class="works-section">
      <b-container-fluid>
        <b-row
          cols="1"
          cols-sm="2"
          cols-md="3"
          cols-lg="4"
        >
          <b-col
            v-for="(work, index) in works"
            :key="work.index"
            :index="index"
            border-variant="dark"
            align="center"
          >
            <!-- <b-col> -->
            <!-- <ArtPreview
                :id="work.index"
                :title="work.title"
                :image="work.image"
              /> -->
            <b-button v-b-modal="`modal-${index}`">
              this works piece from works vue
            </b-button>

            <b-modal :id="`modal-${index}`" centered :title="work.title">
              <p class="my-4">
                Vertically centered modal!
              </p>
              <p>
                this is called {{ work.title }}
              </p>
              inside here place artwork
            </b-modal>
          </b-col>
        </b-row>
      </b-container-fluid>

      <!--
      <div v-for="work in works" :key="work.id">
        <ArtPreview
          :id="work.id"
          :title="work.title"
          :image="work.image"
        />
        <Modal
          :id="work.id"
          :title="work.title"
          :image="work.image"
        />
        <b-button v-b-modal="'modal' + work.id">
          this works piece
        </b-button>
        <b-modal :id="'modal' + work.id" centered title="BootstrapVue">
          <p class="my-4">
            Vertically centered modal!
          </p>
          <p>
            this is called {{ work.title }}
          </p>
          inside here place artwork
        </b-modal>
      </div>
      -->
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      works: [
        {
          title: '1st one',
          image: require('../assets/img/henrik-donnestad-t2Sai-AqIpI-unsplash.jpg'),
          index: '1',
          description: "Pretend you're water. Just floating without any effort. Having a good day. Let's put some happy little clouds in our world. This is truly an almighty mountain. This is a fantastic little painting."
        },
        {
          title: '2nd one',
          image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          index: '2',
          description: "Imagination is the key to painting. Don't fight it, use what happens. It all happens automatically. We're trying to teach you a technique here and how to use it."
        },
        {
          title: 'Third',
          image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          index: '3',
          description: "It's a good way of getting rid of all your anxieties and hostilities. Mountains are so simple, they're hard. Just let your mind wander and enjoy. This should make you happy."
        },
        {
          title: 'The forth!',
          image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          index: '4',
          description: "It's amazing what you can do with a little love in your heart. No worries. No cares. Just float and wait for the wind to blow you around."
        }
      ]
    }
  }
}
</script>

<style>
  .works {
    background-color: rgb(49, 5, 49);
    margin-top: -85px;
  }

  .card {
    background-color: rgb(49, 5, 49);
  }

  .works-section {
    padding-top: 85px;
    margin-right: 20px;
    margin-left: 40px;
  }

  .works-card {
    margin: 10px;
    padding: 10px;
  }

  .work-columns {
    padding: 10px;
  }
</style>
