<template>
  <div id="app">
    <h1>Todo application</h1>
    <TodoList 
      v-bind:todos="todos" 
      @remove-todo="removeTodo"
    />  
    <!--@ - тоже что и v-on-->
  </div>
</template>

<script>
import TodoList from '@/components/TodoList'
export default {
  name: 'App',
  data () {
    return {
      todos: [
            {id:1, title:'Купить хлеб', completed: false},
            {id:2, title:'Купить молоко', completed: false},
            {id:3, title:'Купить картошку', completed: false},
            {id:4, title:'Купить картошку', completed: false},
            {id:5, title:'Купить картошку', completed: false},
            {id:6, title:'Купить картошку', completed: false},
            {id:7, title:'Купить картошку', completed: false}
      ]
    }
  },
  methods: {
    removeTodo(id) {
      this.todos = this.todos.filter(t => t.id !== id)
    }
  },
  components: {
    TodoList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
<!--c помощью метода filter(t => t.id !== id) удаляем элемент из родителя(маccива todos)>