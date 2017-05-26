<template>
  <div id="app">
   <p><h2>Grade Calculator</h2></p>
    <addlist :add="add"></addlist>
    <list-show :lists="lists" :deletelist="deletelist"></list-show>
  </div>
</template>
<script>
import ListShow from './components/ListShow'
import Addlist from './components/Addlist'
export default {
  name: 'app',
  data () {
    return {
      lists: []
    }
  },
  components: {
    ListShow,
    Addlist
  },
  methods: {
    add (name, credit, grade) {
      var data = {
        id: Date.now(),
        name: name,
        credit: credit,
        grade: grade
      }
      this.lists.push(data)
    },
    deletelist (id) {
      var index = this.lists.findIndex(list => list.id === id)
      this.lists.splice(index, 1)
    },
    editList (id, name, surname) {
      var index = this.lists.findIndex(list => list.id === id)
      this.lists[index].name = name
      this.lists[index].surname = surname
      // this.lists[index].grade = grade
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
