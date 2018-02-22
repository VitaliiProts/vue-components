<template>
  <section>
    <h2>{{ message }}</h2>
    <app-input :msg="message" @messChange="message = $event"></app-input>
  </section>
</template>

<script>
import Input from './Field.vue'

  export default {
  data () {
    return {
      message: 'New component Example!'
    }
  },
    components: {
      'app-input': Input
    }
  }
</script>