<template>
  <label :for="label" v-bind="$attrs">{{ label }}</label>
  <input :type="type" :id="label" :name="label" />
</template>

<script>
  export default {
    name: "inputField",
    props: {
      label: {
        type: String,
        required: true,
      },
      type: {
        type: String,
        required: true,
      },
    },
  };
</script>

<style></style>
