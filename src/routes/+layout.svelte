<script>
    import { scale, slide } from "svelte/transition";
  import "../app.css";

  let isNavBarMenuDrawer = false
  const handleNavBarMenuDrawer = ()=>{
    isNavBarMenuDrawer = !isNavBarMenuDrawer
  }
</script>

<svelte:head>
  <title>CheapAli</title>
</svelte:head>

<section class="w-full min-h-screen bg-neutral-300 dark:bg-neutral-900 text-neutral-900 dark:text-neutral-100">

  <slot />
</section>