<template>
<button class="btn btn-primary">
  {{ btnName }}
</button>
</template>

<script>
export default {
  props: {
    btnName: {
      type: String,
      default:"sample btn"
    },
  },
}
</script>

<style scoped>

</style>