<template>
  <div>
    <b-button v-b-modal="'modal' + id" modal-center>
      works piece
    </b-button>
    <b-modal :id="'modal-center' + id" centered title="BootstrapVue">
      <p class="my-4">
        Vertically centered modal!
      </p>
      <p>
        this is called
      </p>
      inside here place artwork
    </b-modal>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
  .preview-image {
    height: 250px;
    width: 250px
  }
</style>
