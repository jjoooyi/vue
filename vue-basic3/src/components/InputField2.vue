<template>
  <div>
    <label for="">Name</label>
    <input 
      type="text" 
      :value="name" 
      style="padding: 30px; border: 2px solid green;"
      @input="$emit('input', $event.target.value)"
    >

  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    }
  },
  methods: {
    updateName(e) {
      this.$emit('update-name', e.target.value)
    }
  }
}
</script>
