<script lang="ts">
    export let title;
</script>

<div class="shadow-md rounded-lg p-5 bg-white">
{#if title !== undefined}
    <h1 class="font-bold pb-2 text-lg">{title}</h1>
{/if}
<slot></slot>
</div>