<script>
    import {addTodo} from "../stores/todoStore";

    let todo = "";

    const handleSubmit = () => {
        addTodo(todo);
        todo = "";
        console.log("todo")
    };

</script>

<form class="my-6" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2 ">
        <label class="font-bold mb-2 text-gray-100" for="todo">ADD TODO</label>
        <input type="text" name="todo" bind:value={todo} placeholder="Type todo here" class="appearance-none border-gray-200 py-3 px-4 focus:outline-none rounded-lg font-semibold bg-[#4A5568] text-gray-100 focus:outline-[#319795]">
    </div>
    <button type="submit" class="w-full rounded bg-[#319795] hover:bg-[#2C7A7B] transition-colors duration-300 text-gray-100 py-2 px-4 font-semibold">ADD</button>
</form>