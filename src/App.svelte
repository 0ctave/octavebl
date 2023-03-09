<script lang="ts">
  import logo from "./assets/svelte.png";
  import Profile from "./lib/Profile.svelte";
  import Context from "./lib/Context.svelte";

</script>

<main class="bg-[url(img)] bg-gray-100 h-full">
    <div class="flex flex-col md:flex-row">
    <div class="basis-2/5">
        <Profile />
    </div>
  <div class="basis-3/5 ">
    <Context />
  </div>
  </div>
</main>
