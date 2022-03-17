<template>
  <li class="list-group-item d-flex justify-content-between">
    {{titleToUppet}}
    <div class="">
      <div class="form-check form-switch">
        <input class="form-check-input" type="checkbox" role="switch" v-model="isDone" :id="'job'+listId">
        <label class="form-check-label" :for="'job'+listId"></label>
      </div>
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
    listId:{
      type:String,
      require:true
    }
  },
  data() {
    return {
      count: 0,
      isDone:true,
    }
  },
  computed: {
    titleToUppet() {
      return this.title.toUpperCase();
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