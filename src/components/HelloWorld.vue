<template>
  <div>
    <index-list :comp_data="comp_data" style="height: 400px;overflow-y: scroll;" @handle_chooseComp_f = "handle_chooseComp_f"></index-list>
  </div>
</template>

<script>
  import IndexList  from 'vue-index-list';
  export default {
    name: 'HelloWorld',
    components: {'index-list': IndexList},
    data () {
      return {
        comp_data: {rows:[['80163340', '安信基金', 'AXJJ'],
          ['80000226', '博时基金', 'BSJJ'],
          ['80510904', '金信基金', 'JXJJ'],
          ['80554846', '南华基金', 'NHJJ']]},
      }
    },
    methods:{
      handle_chooseComp_f(code,name){
        console.log(code);
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
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
