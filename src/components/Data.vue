<template>
    <v-contai>     
    <v-card class="mx-auto" max-width="344" outlined v-for="(item, i) in additems" :key="i" height="100px">
    <v-list-item-content>
        <center><v-list-item-subtitle>{{item.text1}}</v-list-item-subtitle></center><br>
        <v-btn  color="primary"  @click="deleteTodo(index)">ลบ</v-btn>
      </v-list-item-content>
    </v-card>
    </v-contai>
</template>
<script>
export default {
 props: ["additems"],
 methods: {
    deleteTodo(index){
      this.additems.splice(index,1);
    },
  },
};
</script>

<style></style>
