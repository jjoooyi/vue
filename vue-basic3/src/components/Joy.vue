<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ name }}{{ age }}</p>
    <button @click="updateName">Change</button>
  </div>  
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'default title',
      //required: true
    },
    age: {
      type: Number,
      default: 20,
    }
  },
  data() {
    return {
      name: 'JOY'
    }
  },
  methods: {
    updateName() {
      this.name = 'Joy updated'
    }
  }
}
</script>

<style scoped>

</style>