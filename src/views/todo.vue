<template>
 <v-continer>
   <h3>Assignments</h3>
  <Input @Addata="addTodo"></Input>
  <Data :additems="additems"></Data>
 </v-continer>
</template>

<script>
import Input from '../components/Input.vue';
import Data from '../components/Data.vue';
export default { 
  data: () =>  ({
      additems: [],
    }),
  additems:"Addata",
  methods:{
    addTodo(subject,work,Time) {
      this.additems.push({
        text1 : subject + " | " + work+ " | "+Time,
      });
    },
  },
 components: { Data,Input },
};
</script>

<style></style>
