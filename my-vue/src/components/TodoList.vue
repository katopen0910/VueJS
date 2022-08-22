<template>
    <div>
        <ul>
            <TodoItem 
                v-for="todo of todos"
                v-bind:todo="todo" 
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