<template>
  <div class="container">
    <div class="row my-3">
      <div class="col-6 mx-3">
        <div class="card">
          <div class="card-body">
            <h1>Hello</h1>
            <p>Lorem Ipsum is simply ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            <Button btn-name="save" is-loading="true"></Button>
          </div>
        </div>
      </div>
      <div class="col-4 mx-3">
        <ul class="list-group">
         <List v-for="list in lists" :key="list.id" :title="list.title"></List>

        </ul>
      </div>
    </div>

  </div>
</template>

<script>

import Button from "@/components/Button";
import List from "@/components/List";
export default {
  components: {List, Button},
  data() {
    return {
      lists: [
        {
          id:1,
          title:"hello",
        },
        {
          id:2,
          title:"hi",
        },
      ]
    }
  },
}
</script>

<style scoped>

</style>