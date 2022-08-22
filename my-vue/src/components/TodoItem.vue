<template>
    <li>
       <span>
        <input type="checkbox">
        <strong>{{todo.id}}</strong>
        {{todo.title}}
       </span>
       <button class="rm">&times;</button>
    </li>
</template>

<script>
    export default { 
        props: {
            todo: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped>/*scoped позволяет быть видным тилям только внутри компонента*/
    li{
        border:1px solid #ccc;
        display: flex;
        justify-content: space-between;
        padding: .5rem 2rem;
        margin-bottom: 1rem;
    }
    input{
        margin-right: 1rem;
    }
    .rm{
        background: red;
        color: #fff;
        border-radius: 50%;
        font-weight: bold;
    }
    .done{
        text-decoration: line-through;
    }
</style>