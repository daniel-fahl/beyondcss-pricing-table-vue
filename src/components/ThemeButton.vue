<script setup>
const props = defineProps({
  inverted: {
    type: Boolean,
    default: false,
    required: false
  }
});
</script>

<template>
  <button :data-state="inverted ? 'inverted' : ''">
    <slot></slot>
  </button>
</template>

<style lang="scss" scoped>
@use "../sass/abstracts" as *;

button {
  cursor: pointer;
  padding: 1em 1.5em;
  font-weight: fw(bold);
  text-transform: uppercase;
  background-color: clr(primary, 400);
  color: clr(neutral, 100);
  border: none;

  justify-self: center;

  &:hover,
  &:focus {
    background-color: rgb(clr(primary, 400), 0.7);
  }

  &[data-state="inverted"] {
    background-color: clr(neutral, 100);
    color: clr(primary, 400);

    &:hover,
    &:focus {
      background-color: rgb(clr(neutral, 100), 0.7);
    }
  }
}
</style>
