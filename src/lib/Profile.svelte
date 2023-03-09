<script lang="ts">
  import Container from "./Container.svelte";
  import profile from '../assets/profile.json';

  import { Icon, ArrowUp, Filter } from "svelte-hero-icons";

</script>

<div class="space-y-5 p-3">

<div class="shadow-md rounded-lg bg-white overflow-hidden">
        <div class="relative w-full">
            <img class="z-0 w-full" src="https://www.radiofrance.fr/s3/cruiser-production/2022/06/5f6ac5ab-37d9-4ca6-8f79-3694fcfec071/560x315_paysage-monet.webp"/>
            <div class="absolute bottom-0 left-0 z-10 w-1/4">
                <img class="border-4 rounded-tr-lg overflow-hidden bg-white" src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Circle-icons-profile.svg" />
            </div>
        </div>
    <div class="p-5 z-10">
        <div class="flex flex-wrap w-full">
            <span class="font-bold">{profile.name}</span>
            <p class="break-all">{profile.description}</p>
        </div>
    </div>
</div>

<Container title="Information">
    <ul>
    	{#each profile.infos as info}
        <li class="flow-root"><span class="float-left text-grey-100">{info.name}</span><span class="float-right font-bold">{info.content}</span></li>
        {/each}
    </ul>
</Container>

<Container title="Skills">
    <div class="flex flex-wrap">
    	{#each profile.skills as skill}
            <span class="bg-blue-200 text-blue-900 p-2 rounded-lg text-sm m-1 hover:animate-pulse"><a href="{skill.ref}">#{skill.name}</a></span>
        {/each}
        </div>
</Container>
</div>