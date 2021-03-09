<template>
  <div class="contact">
    <h1 class="contact-title text-center">
      Say hi!
    </h1>
    <b-form class="contact-form" @submit="onSubmit" @reset="onReset">
      <b-form-group id="input-group-1" label="name" label-for="input-1">
        <b-form-input id="input-1" v-model="form.name" type="text" required placeholder="Bilbo Baggins" />
      </b-form-group>
      <b-form-group id="input-group-2" label="email" label-for="input-2">
        <b-form-input id="input-2" v-model="form.email" type="email" required placeholder="bilbobaggins@theshire.com" />
      </b-form-group>
      <b-form-group id="input-group-3" label="message" label-for="input-3">
        <b-form-textarea
          id="input-3"
          v-model="form.message"
          type="text"
          required
          placeholder="Say Hi!"
          rows="3"
          max-rows="6"
        />
      </b-form-group>
      <b-button pill variant="outline-dark">
        Submit
      </b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      form: {}
    }
  },
  methods: {
    onSubmit () {},
    onReset () {}
  }
}
</script>

<style>
  .contact {
    margin-top: -75px;
    padding-left: 160px;
    padding-right: 160px;
    padding-top: 100px;
    background-color: rgb(165, 136, 136);
    height: 100vh;
  }

  .contact-title {
    font-family: Abril Fatface, cursive;
  }

  .contact-form {
    padding-top: 10px;
  }
</style>
