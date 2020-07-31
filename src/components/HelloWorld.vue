<template>
  <div class="hello">
    
    <ul>
      <li v-for="(item,index) in list" :key="item.id"> <span>{{item.id}}</span> <input type="checkbox" ><button @click="del(index)">del</button>  </li>
    </ul>
  </div>
</template>

<script>
// Diff
export default {
  name: 'HelloWorld',
  data () {
    return {
      list:[{
        id:1,
        text:"a"
      },{
        id:1,
        text:"b"
      },{
        id:3,
        text:"c"
      }]
    }
  },
  methods:{
    del(i){
      this.list.splice(i,1);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
