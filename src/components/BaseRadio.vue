<template>
  <input
    type="radio"
    class="h-5 w-5 cursor-pointer"
    :id="id"
    v-bind="$attrs"
    v-model="value"
  />
  <label v-if="$slots.default" :for="id" class="pl-4 cursor-pointer flex-grow">
    <slot />
  </label>
</template>

<script>
export default {
  props: {
    id: String,
    modelValue: String
  },
  data() {
    return {
      value: ''
    }
  },
  mounted() {
    this.value = this.modelValue
  }
}
</script>
