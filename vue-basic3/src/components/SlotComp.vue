<template>
  <div>
  <p>header</p>
  <slot name="header" :joy="joy"></slot>
  <p>body</p>
  <slot :joy="joy"></slot>
  <p>footer</p>
  </div>  
</template>

<script>
export default {
  data() {
    return {
      joy: 'hahah'
    }
  }
}
</script>

<style scoped>

</style>