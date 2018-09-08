<template>
  <label>
    <select :value="value"
            @input="$emit('input', $event.target.value)">
      <option v-for="(item, key) in list" :key="key" :value="key">{{ item.name }}</option>
    </select>
  </label>
</template>

<script>
export default {
  name: 'MySelect',
  props: ['value', 'list'],
};
</script>

<style scoped>

</style>
