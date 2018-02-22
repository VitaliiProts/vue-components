<template>
  <section>
    <h3>This is Field!</h3>
    <input type="text" :value="msg" @input="changeMess">
    <p>{{ mess }}</p>
  </section>
</template>

<script>
  export default {
    data () {
      return {
        mess: ''
      }
    },
    methods: {
      changeMess: function (event) {
        this.mess = event.target.value;
        this.$emit('messChange', this.mess);
      }
    },
    props: ['msg']
  }
</script>