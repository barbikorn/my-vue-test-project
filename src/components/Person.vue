<template>
  <li>
    <h3>ชื่อ : {{name}}</h3>
    <div class="button-container">
      <button  v-if="isVisible===false" @click="showDescription(tel)">ดูรายละเอียด</button>
      <button v-if="isVisible===true">ปิดรายละเอียด</button>
      <button>ลบข้อมูล</button>
    </div>
    <div v-show="isVisible">
        <p>tel : {{tel}}</p>
        <p>department : {{department}}</p>
    </div>
  </li>

  
</template>

<script>


export default {
  name: 'PersonComponent',
  data(){
    return{
      description : "List data component",
      message :  "ข้อมูลพนักงาน"
    }
  },
  methods:{
    showDescription(tel){
      console.log(tel)
    }
  },
  props:{
    name:{
        type:String,
        required:true
    },
    tel:{},
    department:{}
  }
}
</script>

<style scoped>
  li{
    margin:1rem 0;
    font-size:1.25rem;
    font-weight:bold;
    background:#8ddba4;
    padding: 0.5rem;
    color : #1f1f1f;
    border-radius : 25px;
  }
  button{
    font:inherit;
    cursor:pointer;
    border:1px solid #ff0077;
    background: #ff0077;
    color: white;
    padding: 0,05rem 1rem;
    box-shadow: 1px 1px 2px rgba(0,0,0,alpha)
  }
  .button-container{
    display: flex;
    column-gap: 20px;
    justify-content: flex-start
  }
</style>
