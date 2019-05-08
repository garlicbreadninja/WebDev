<template>
  <div id="app">
    <Header />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
import Todos from './components/Todos';
import Header from './components/layout/Header'
import AddTodo from './components/AddTodo'
export default {
  name: 'App',
  components: {
    Todos, Header, AddTodo
  },
  data() {
    return {
     todos: [
       {
         id: 1,
         title: "Todo one",
         completed: false
       },
       {
         id: 2,
         title: "Todo two",
         completed: false
       },
       {
         id: 3,
         title: "Todo three",
         completed: false
       }
     ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    },
    addTodo(newTodo){
      this.todos = [...this.todos, newTodo];
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
 .btn{
   display: inline-block;
   border: none;
   background: #555;
   color: #fff;
   padding: 7px 20px;
   cursor: pointer;
 }
 .btn:hover{
   background: #666;
 }
</style>
