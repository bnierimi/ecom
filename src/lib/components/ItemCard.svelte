<script>
  export let name = ""
  export let newPrice = ""
  export let oldPrice = ""
  export let imgSrc = ""
  export let url = ""
</script>

<a href="/p/{url}" class="focus:outline-none focus:ring-2 focus:ring-amber-500 rounded-lg">
  <section class="h-64 rounded-lg flex flex-col justify-between group hover:cursor-pointer bg-neutral-100 dark:bg-neutral-800 dark:hover:bg-neutral-700 shadow-md shadow-transparent hover:shadow-neutral-400/20 dark:hover:shadow-neutral-900/20 ">
    <div class="w-full space-y-1">
      <div class="w-full h-44 bg-neutral-100 rounded-lg overflow-hidden">
        <img src={imgSrc} alt="CheapAli'sbanner" class="w-full h-full object-cover">
      </div>
      <h5 class="font-medium px-3 w-full text-ellipsis">{name}</h5>
    </div>
    <div class="flex items-center justify-between p-3">
      <p class="font-medium text-lg ">{newPrice}</p>
      <p class="line-through text-rose-600">{oldPrice}</p>
    </div>
  </section>
</a>