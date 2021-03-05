<template>
  <div class="works">
    Works!
    <div class="works-section">
      <!-- <ArtPreview
        v-for="work in works"
        :id="work.id"
        :key="work.id"
        :title="work.title"
        :image="work.image"
      /> -->
      <!-- <Modal
        v-for="work in works"
        :id="work.id"
        :key="work.id"
        :title="work.title"
        :image="work.image"
      /> -->
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
        <!-- <b-button v-b-modal.modal-1> -->
        <b-button v-b-modal="'modal' + work.id">
          this works piece
        </b-button>
        <b-modal :id="'modal' + work.id" centered title="BootstrapVue">
          <!-- <b-modal id="modal" centered title="BootstrapVue"> -->
          <p class="my-4">
            Vertically centered modal!
          </p>
          <p>
            this is called {{ work.title }}
          </p>
          inside here place artwork
        </b-modal>
      </div>
      <!-- <b-button v-b-modal.modal-center>
        works piece
      </b-button>
      <b-modal :id="'modal-center-' + work.id" centered title="BootstrapVue">
        <p class="my-4">
          Vertically centered modal!
        </p>
        <p>
          this is called {{ title }}
        </p>
        inside here place artwork
      </b-modal> -->
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
          id: '1'
        },
        {
          title: '2nd one',
          image: require('../assets/img/europeana-VsnDYMWollM-unsplash.jpg'),
          id: '2'
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

  .works-section {
    padding-top: 85px;
  }
</style>
