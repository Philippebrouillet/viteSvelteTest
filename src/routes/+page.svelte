<script>
  import AddTodoSection from "../lib/components/todo/AddTodoSection.svelte";
  import TodoSection from "../lib/components/todo/TodoSection.svelte";
  import ProgressSection from "../lib/components/progress/ProgressSection.svelte";
</script>

<div class="min-h-screen p-0 selection:bg-green-300 md:px-8 md:py-24">
  <main
    class="md:outline-cream-1 mx-auto min-h-screen max-w-none rounded-none bg-yellow-50 py-10 outline-none md:min-h-max md:max-w-[60rem] md:rounded-2xl md:px-8 md:outline md:outline-4 md:outline-offset-8"
  >
    <h1 class="text-2xl font-bold ">TodoList</h1>
    <div class="mt-10" />
    <div>
      <AddTodoSection />
      <TodoSection />
      <ProgressSection/>
    </div>
  </main>
</div>
