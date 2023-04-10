<script>
  import { deleteTodo, toggleComplete, editTodo } from "../../store/TodoStore";

  export let todo;
  
  $: completeClass = todo.complete ? "bg-green-300" : "bg-blue-300";
</script>

<div
  class="flex items-center justify-between rounded-md border-2 border-gray-300 px-5 py-4"
>
  <div class="flex w-full max-w-lg items-center justify-start">
    <label for={`${todo.id}-checkbox`} class="sr-only">Complete todo</label>
    <input
      on:change={() => toggleComplete(todo.id)}
      checked={todo.complete}
      type="checkbox"
      id={`${todo.id}-checkbox`}
      class="h-4 w-4 rounded border cursor-pointer border-gray-300 text-green-400 focus:border-green-500 focus:outline focus:outline-2 focus:outline-offset-2 focus:outline-green-200"
    />
    <label
      class="sr-only"
      for={`${todo.id}-text`}>Edit todo</label
    >
    <input
      type="text"
      class="text-gray-500 bg-yellow-50 mx-5 flex-1 text-ellipsis rounded-md border-x-0 border-b border-t-0  border-b-gray-200 px-2 pb-1 text-base font-normal placeholder:text-gray-400 focus:border-gray-300 focus:outline-none focus:ring-0"
      id={`${todo.id}-text`}
      placeholder="Enter a todo"
      value={todo.text}
      on:input={(e) => editTodo(todo.id, e.target.value)}
    />

    <span class="{completeClass} ml-5 hidden rounded-full py-0.5 px-2 font-normal text-sm text-gray-500 md-block">{todo.complete ? "Complete" : "In progress"}</span>
    <button
      type="button"
      class="rounded-lg border-2 bg-gray-300 p-1 text-white hover:scale-[105%]"
      on:click={() => deleteTodo(todo.id)}
    >
      <span class="">Delete</span></button
    >
  </div>
</div>
