<template>
  <h1>{{description}}</h1>
  <ul>
    <Person v-for="(person, index) in personData"
      :key="index" 
      :name="person.name" 
      :tel="person.tel" 
    />
  </ul>

</template>

<script>
import Person from './Person'

const personData = [
    {
      name : "Jim",
      tel:"0875551234",
      department : "พนักงาน",
      isVisible:false
    },
    {
      name : "Thomas",
      tel:"0875551234",
      department : "การตลาด",
      isVisible:false
    },
    {
      name:200,
      tel:"0655555555",
      department : "จัดซื้อ",
      isVisible:false
    }
  ]


export default {
  name: 'ListData',
  components:{Person},
  data(){
    return{
      description : "List data component",
      message :  "แสดงรายชื่อพนักงาน",
      personData : personData 
    }
  },
}
</script>

<style scoped>
  ul{
    color:green
  }
</style>
