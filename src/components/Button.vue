<template>
  <button class="btn btn-primary" type="button" disabled>
    <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
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
    isloading:{
      type: Boolean,
      default: false
    }
  },
}
</script>

<style scoped>

</style>