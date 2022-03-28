<script>
    import TodoForm from "../components/TodoForm.svelte";
    import Todo from "../components/Todo.svelte";
    import {todos} from "../stores/todoStore";
</script>

<main>
    <h1 class="text-2xl text-center font-bold text-gray-100 md:text-3xl">TODOS</h1>
    <TodoForm />
    {#each $todos as todo}
        <Todo todo={todo} index={todos.id} />
    {/each}
</main>