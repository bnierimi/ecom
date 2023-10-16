<script>
  export let name = ""
  export let newPrice = ""
  export let oldPrice = ""
  export let imgSrc = ""
</script>

<section class="h-64 rounded-lg flex flex-col justify-between group hover:cursor-pointer bg-neutral-200/30 hover:bg-neutral-200/80 dark:bg-neutral-800/30 dark:hover:bg-neutral-800/80 shadow-md shadow-transparent hover:shadow-neutral-400/20 dark:hover:shadow-neutral-800/20 ">
  <div class="w-full space-y-1">
    <div class="w-full h-44 bg-neutral-100 rounded-lg overflow-hidden">
      <img src={imgSrc} alt="CheapAli'sbanner" class="w-full h-full object-cover">
    </div>
    <h5 class="font-medium px-3 w-full text-ellipsis">{name}</h5>
  </div>
  <div class="flex items-center justify-between p-3">
    <p class="font-medium text-lg">{newPrice}</p>
    <p class="line-through text-rose-600">{oldPrice}</p>
  </div>
</section>