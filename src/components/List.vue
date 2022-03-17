<template>
  <li class="list-group-item d-flex justify-content-between">
    <div class="" @dblclick="edit">
      <span v-if="isEdit">
      <input type="text" class="form-control" v-model="listItem.title">
    </span>
      <span v-else>
          {{titleToUppet}}
    </span>
    </div>

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
      isEdit:true
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
    },
    edit(){
      this.isEdit= !this.isEdit;
    }
  },
}
</script>

<style scoped>

</style>