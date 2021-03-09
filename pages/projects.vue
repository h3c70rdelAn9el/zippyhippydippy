
<template>
  <div class="works">
    <b-container fluid class="works-section">
      <h1 class="works-title">
        Works
      </h1>
      <b-row
        cols="1"
        cols-sm="2"
        cols-md="3"
        cols-lg="4"
        class="work-rows"
      >
        <b-col
          v-for="(work, index) in works"
          :key="work.index"
          :index="index"
          border-variant="dark"
          align="center"
          class="work-columns d-flex flex-column align-items-center"
        >
          <p>
            {{ work.title }}
          </p>
          <img class="work-image" :src="work.image" alt="">
          <b-button v-b-modal="`modal-${index}`" class="work-button">
            See more..
          </b-button>

          <!-- Modal -->
          <b-modal :id="`modal-${index}`" size="md" :title="work.title" centered hide-footer>
            <ProjectPreview
              :title="work.title"
              :image="work.image"
              :description="work.description"
              :index="work.index"
            />
          </b-modal>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      works: [
        {
          title: 'Opus 1',
          image: require('../assets/img/henrik-donnestad-t2Sai-AqIpI-unsplash.jpg'),
          index: '1',
          description: "Pretend you're water. Just floating without any effort. Having a good day. Let's put some happy little clouds in our world. This is truly an almighty mountain. This is a fantastic little painting."
        },
        {
          title: 'Etude 204',
          image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          index: '2',
          description: "Imagination is the key to painting. Don't fight it, use what happens. It all happens automatically. We're trying to teach you a technique here and how to use it."
        },
        {
          title: 'Waiting',
          // image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          image: require('../assets/img/tim-mossholder-hrm0hf8pCdU-unsplash.jpg'),
          index: '3',
          description: "It's a good way of getting rid of all your anxieties and hostilities. Mountains are so simple, they're hard. Just let your mind wander and enjoy. This should make you happy."
        },
        {
          title: 'Paleness',
          image: require('../assets/img/steve-johnson-e5LdlAMpkEw-unsplash.jpg'),
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
    color: white;
  }

  .card {
    background-color: rgb(49, 5, 49);
  }

  .works-section {
    padding-top: 85px;
    margin-right: 20px;
    align-items: center;
  }

  .works-card {
    margin: 10px;
    padding: 10px;
  }

  .work-rows {
    margin: 5px;
  }

  .work-columns {
    padding: 10px;
  }

  .modal-content {
    background-color: rgb(49, 5, 49);
    color: gray;
    align-items: center;
  }

  .work-image {
    height: 170px;
    width: 170px;
    border-radius: 10px;
  }

  .modal-header {
    width: 100%;
  }

  .modal-header {
    text-align: center;
  }

  .work-button {
    margin-top: 10px;
  }

  .works-title {
    text-align: center;
    color: rgb(192, 182, 182);
    margin-top: 10px;
    font-family: Abril Fatface, cursive;
  }
</style>
