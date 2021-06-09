<template>
  <div>
    <h1>This is Home page</h1>

    <form action="">
      <InputField :name="name" @update-name="name = $event.target.value" />
      {{ name }}
      <InputField2 v-model="name2" />
      {{ name2 }}
      <br><button>submit</button>
    </form>
  </div>  
</template>

<script>
import InputField from '@/components/InputField.vue'
import InputField2 from '@/components/InputField2.vue'
export default {
  components: {
    InputField,
    InputField2
  },
  data() {
    return {
      name: '',
      name2: ''
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
