<template>
  <label>
    <select v-model="optionValue" @change="sendingEvent">
      <option v-for="(item, key) in list" :key="key" :value="key">{{ item.name }}</option>
    </select>
  </label>
</template>

<script>
export default {
  name: 'MySelect',
  props: ['list'],
  data() {
    return {
      optionValue: 0,
    };
  },
  methods: {
    sendingEvent() {
      this.$emit('parent-change-city', this.optionValue);
    },
  },
};
</script>

<style scoped>

</style>
