<template>
  <li class="list-group-item d-flex justify-content-between">
    {{title}}
    <div class="">
      <button class="btn btn-sm btn-primary me-2" @click="countIncrement">+</button>
      <span>
        {{count}}
      </span>
    </div>

  </li>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "Default"
    },
  },
  data() {
    return {
      count: 0
    }
  },
  computed: {
    title() {
      return this.data 
    }
  },
  methods: {
    countIncrement() {
      this.count++;
    }
  },
}
</script>

<style scoped>

</style>