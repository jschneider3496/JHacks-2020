<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Wlcome to Your Vue.js App"/>
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'

import {ItemList} from './backend/ItemList.js'
import {ToDoItem} from './backend/ItemList.js'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}

var itemList = new ItemList();

itemList.add(new ToDoItem("h",false,"g", 10));
itemList.add(new ToDoItem("b",false,"g", 1));
itemList.add(new ToDoItem("d",false,"g", 130));
// console.log("ggg")
console.log(itemList.printList());

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
