<template>
  <v-sheet>
    <h3>نام برنامه</h3>
    <v-row>
      <v-col cols="8">
        <v-textarea
          label="برنامه شماره1"
          outlined
          height="50px"
          class="textarea my-8"
        ></v-textarea>
      </v-col>
    </v-row>
  </v-sheet>
</template>
  
  <style scoped>
.textarea {
  padding-right: 18em;
  padding-left: 20em;
}
h3 {
  padding-right: 15em;
  padding-top: 2em;
}
</style>

<script>
export default {
  name: "TopRowComponent",
};
</script>
<style>
body {
  font-family: Helvetica, Arial;
}
</style>


  
  
  
  
  
  
  