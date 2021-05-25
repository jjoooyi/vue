<template>
  <div>
    <h2>{{ title }}</h2>
    <p>{{ name }}</p><br>
    <button @click="updateName">Change name</button>
  </div>
</template>

<script>
export default {
  // props: ['title'],
  props: {
    title: {
      type: String,
      default: 'default title',
      required: false
    },
    name: {
      type: String,
      default: 'default name'
    }
  },
  data() {
    return {
      // name: 'Jooyi Coder'
    }
  },

  methods: {
    updateName() {
      this.name = 'Jooyi Coder Updated' //자식컴포넌트에서 props 값을 변경하면 안됨! 부모컴포넌트에서 수정할 수 있도록 해야한다!
    }
  }
}
</script>

<style scoped>

</style>