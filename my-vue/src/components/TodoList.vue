<template>
    <div>
        <ul>
            <TodoItem 
                v-for="(todo, i) of todos"
                :key="todo.id"
                v-bind:todo="todo"
                 v-bind:index="i"
                v-on:remove-todo="removeTodo"
            />
        </ul>
    </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'
export default {
    props: ['todos'],
    components: {
        TodoItem
    },
    methods: {
        removeTodo(id) {
          this.$emit('remove-todo', id)  
        }
    }
}
</script>

<style scoped>/*scoped позволяет быть видным тилям только внутри компонента*/
ul{
    list-style-type: none;
    margin: 0;
    padding: 0;
}
</style>             
              