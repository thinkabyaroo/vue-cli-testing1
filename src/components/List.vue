<template>
  <li class="list-group-item d-flex justify-content-between">
    {{titleToUppet}}
    <div class="">
      <div class="form-check form-switch">
        <input class="form-check-input" type="checkbox" @change="$emit('changeStatus',listItem.id)" role="switch" v-model="isDone" :id="'job'+listItem.id">
        <label class="form-check-label" :for="'job'+listItem.id"></label>
      </div>
    </div>

  </li>
</template>

<script>
export default {
  props: {
   listItem:{
     type:Object
   }
  },
  data() {
    return {
      count: 0,
      isDone:this.listItem.isDone,
    }
  },
  computed: {
    titleToUppet() {
      return this.listItem.title.toUpperCase();
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