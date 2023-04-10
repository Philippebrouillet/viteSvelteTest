<script>
    import {addTodo} from '../../store/TodoStore'
</script>

<section class='flex justify-between'>
    <h3 class="text-xl font-bold text-gray-three">Checklist</h3>
    
    <button type="button" class='border-2 rounded-lg p-1 bg-gray-300 hover:scale-[105%] text-white' on:click={addTodo}>Add Task</button>
</section>