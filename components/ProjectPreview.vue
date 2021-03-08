<template>
  <div class="art-preview d-flex flex-column align-items-center">
    <img :src="image" alt="" class="preview-image">
    <p>{{ description }}</p>
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
    index: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
  .art-preview {
    background-color: rgb(49, 5, 49);
    color: gray;
  }

  .art-title {
  }

  .preview-image {
    height: 300px;
    width: 300px
  }
</style>
