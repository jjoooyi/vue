<template>
  <div class="about">
    <h1>This is an about page</h1>
    <SlotComp>
      <template #header="props">
        <p>v-slot:header == #header {{ props.joy }}</p>
      </template>
      hello1
      <template #default="{ joy }">
        hohoho {{ joy }}
      </template>
    </SlotComp>
    <Joy title="About title" />
  </div>
</template>

<script>
import Joy from '@/components/Joy.vue';
import SlotComp from '@/components/SlotComp.vue';
export default {
  components: {
    Joy,
    SlotComp
  }
}
</script>
