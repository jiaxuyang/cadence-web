<template>
  <div class="text-input field">
    <input
      :disabled="disabled"
      :name="name"
      placeholder=" "
      :readonly="readonly"
      :type="type"
      :value="value"
      @input="onInputChange"
    />
    <label :for="name">{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: 'text-input',
  props: ['disabled', 'label', 'name', 'readonly', 'type', 'value'],
  methods: {
    onInputChange(...args) {
      this.$emit('input', ...args);
    },
  },
};
</script>

<style lang="stylus">
@require "../styles/base.styl"
</style>
