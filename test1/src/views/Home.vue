<template>
  <div>
    <h1>This is Home page</h1>
    <hr>
    <JooyiCoder title="home title" name="jooyi coder" />
    <hr>
    <form action="">
      <InputField :name="name" @update-name="updateName"/>
      <br><button>Submit</button>
    </form>
    {{ name }}
  </div>
</template>

<script>
import JooyiCoder from '@/components/JooyiCoder.vue'
import InputField from '@/components/InputField.vue'

export default {
  components: {
    JooyiCoder,
    InputField
  },
  data() {
    return {
      name: ''
    }
  },
  methods: {
    updateName(name) {
      this.name = name;
    }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>