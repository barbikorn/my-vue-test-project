<template>
  <h1>{{description}}</h1>
</template>

<script>


export default {
  name: 'FormComponent',
  data(){
    return{
      description : "Form component"
    }
  }
}
</script>

<style scoped>
  h1{
    color:red;
  }
</style>

