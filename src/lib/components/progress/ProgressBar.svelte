<script>
    export let title;
    export let percentage
    $: completeClass = title === 'Completed' ? 'bg-green-300' : 'bg-gray-400'
</script>


<div>
    <div class="flex justify-between text-base font-normal text-gray-500 ">
        <p>{title}</p>
        <p>{percentage}%</p>
    </div>
    <div class="mt-5 w-full overflow-hidden rounded-full">
        <div class="{completeClass} h-4 rounded-full transition-all duration-500 ease-out" style="width: {percentage}%"/>
    </div>
</div>