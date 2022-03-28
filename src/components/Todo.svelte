<script>
    import { deleteTodo, toggleTodo } from "../stores/todoStore";

    export let todo;
</script>

<li class="flex items-center border-2 border-[#319795] rounded-lg my-2 py-2 px-4">
    <input type="checkbox" name="completed" checked={todo.completed} on:change={() => toggleTodo(todo.id)} class="mr-2 form-checkbox h-6 w-6 appearance-none border-2 focus:outline-none rounded-md border-[#319795] checked:border-[#81E6D9] checked:bg-[#81E6D9]">
    <span class={`flex-1 text-gray-100 text-lg font-base ${todo.completed ? "line-through" : ""}`}>{todo.text}</span>
    <button type="button" class="text-sm font-semibold bg-red-500 hover:bg-red-600 transition-colors duration-300 text-gray-100 py-1 px-2 rounded focus:outline-none" on:click={() => deleteTodo(todo.id)}>DELETE</button>
</li>