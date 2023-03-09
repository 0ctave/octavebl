<script>
  import Container from "./Container.svelte";
  import profile from '../assets/profile.json';

   let tab = profile.context[0];
</script>

<div class="space-y-5 p-3">




    <div class="px-2 pt-1 pb-0.5 shadow-md rounded-lg bg-white">
        <ul class="inline">
            	{#each profile.context as section}
                    <li class:border-b-4={tab == section} class="inline hover:border-b-4 px-2 hover:border-blue-900 border-blue-700"><button on:click={() => tab = section}>{section.name}</button></li>
                {/each}
        </ul>
    </div>
    <p>{tab.name}</p>
        {#each tab.content as container}
            <Container title="{container.title}">
                <p>fsffsfs</p>
            </Container>
        {/each}
</div>