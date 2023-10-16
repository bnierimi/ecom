<script>
  import ItemCard from "$lib/components/ItemCard.svelte";
  import { slide } from "svelte/transition";

  const listOfCatergories = [
    "Watches",
    "Phone accessories",
    "Gadgets and Electronics",
    "Laptop accessories",
    "Place an Aliexpress Order",
  ]
  const listOfProducts = [
    "Watches",
    "Phones",
    "Glasses",
    "Camera",
  ]
  const listOfItems = [
    {
      name: "iPhone 15 leather case",
      newPrice: "$179.99",
      oldPrice: "$279.99",
      imgSrc: "/images/iphone-15-case.jpg"
    },
    // {
      //   name: "Ads: Shop at CheapAli",
    //   newPrice: "www.cheapali.com",
    //   oldPrice: "",
    //   imgSrc: "/images/banner.jpg"
    // },
    {
      name: "Women's Luxury watch",
      newPrice: "$79.99",
      oldPrice: "$99.99",
      imgSrc: "/images/watch1.jpg"
    },
    {
      name: "iPhone 11 case",
      newPrice: "$99.99",
      oldPrice: "$109.99",
      imgSrc: "/images/iphone-11-case.jpg"
    },
    {
      name: "Men's Package watch",
      newPrice: "$19.99",
      oldPrice: "$79.99",
      imgSrc: "/images/watch4.jpg"
    },
    {
      name: "Samsung S20 case",
      newPrice: "$19.99",
      oldPrice: "$79.99",
      imgSrc: "/images/samsung-s20-case.jpg"
    },
  ]

  let isNavBarMenuDrawer = false
  const handleNavBarMenuDrawer = ()=>{
    isNavBarMenuDrawer = !isNavBarMenuDrawer
  }
</script>

<nav class="w-full p-4 flex items-center justify-between bg-neutral-100 dark:bg-neutral-800">
  <a href="/" class="">
    <div class="">
      <img src="/images/cheapali-logo.png" alt="" class="w-14">
    </div>
  </a>
  
  <section class="flex items-center space-x-3">
    <div class="flex items-center space-x-1 rounded-full border-none dark:bg-neutral-700 bg-neutral-300 focus-within:border-amber-600">
      <i class="pl-3 pr-1.5">Q</i>
      <input type="text" name="searchInput" id="searchInput" placeholder="Search CheapAli" class="w-full bg-transparent bborder-none focus:border-none focus:outline-0 focus:ring-0 rounded-full py-2 pr-2 text-sm">
      <!-- <button class="p-2 rounded-lg bg-amber-600 hover:bg-amber-700 font-medium">Q</button> -->
    </div>

    <section class="flex">
      <button on:click={handleNavBarMenuDrawer} class="flex px-2.5 pb-1b bg-neutral-200 hover:bg-neutral-300 dark:bg-neutral-800 dark:hover:bg-neutral-700 rounded-md">
        <i class="icon icon- flex text-3xl font-bold">&equiv;</i>
      </button>
      
      {#if isNavBarMenuDrawer}
        <div class="w-full h-full fixed top-0 right-0 z-20">
          <div on:click={handleNavBarMenuDrawer} class="w-full h-full absolute bg-transparent/80"/>

          <section transition:slide={{axis: 'x'}} class="fixed top-0 right-0 z-40 h-full w-11/12 md:w-96  rounded-l-lg bg-neutral-100 dark:bg-neutral-900 pt-4 pb-1 px-1 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-900/20 space-y-2">
            <div class="flex items-center justify-between px-4">
              <h3 class="font-medium text-lg">CheapAli</h3>

              <button on:click={handleNavBarMenuDrawer} class="flex px-1.5 pb-1 bg-neutral-200 hover:bg-neutral-300 dark:bg-neutral-800 dark:hover:bg-neutral-700 rounded-md">
                <p class="icon icon- flex text-3xl font-bold">&xotime;</p>
              </button>
            </div>
            <ul class="w-full space-y-1">
              <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 rounded-lg ">
                <img src="/logos/github.svg" alt="icon" class="w-7">
                <span class="">[Cart]</span>
              </a></li>
              <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 rounded-lg ">
                <img src="/logos/github.svg" alt="icon" class="w-7">
                <span class="">Home</span>
              </a></li>
              <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 rounded-lg ">
                <img src="/logos/github.svg" alt="icon" class="w-7">
                <span class="">About</span>
              </a></li>
              <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 rounded-lg ">
                <img src="/logos/github.svg" alt="icon" class="w-7">
                <span class="">Contact</span>
              </a></li>
            </ul>
          </section>
        </div>
      {/if}
    </section>
  </section>
</nav>

<section class="w-full h-full p-4 md:flex md:space-x-4 relative">
  <aside class="hidden lg:block h-full  w-3/12 sticky top-4 space-y-4">
    <section class="w-full rounded-lg bg-neutral-100 dark:bg-neutral-800 pt-4 pb-1 px-1 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20 space-y-2">
      <h3 class="font-medium text-lg px-3">Products</h3>
      <ul class="w-full space-y-1">
        {#each listOfProducts as eachProduct}
          <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-700 rounded-lg ">
            <img src="/logos/github.svg" alt="icon" class="w-7">
            <span class="">{eachProduct}</span>
          </a></li>
        {/each}
      </ul>
    </section>
    
    <section class="w-full rounded-lg bg-neutral-100 dark:bg-neutral-800 pt-4 pb-1 px-1 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20 space-y-2">
      <h3 class="font-medium text-lg px-3">Categories</h3>
      <ul class="w-full space-y-1">
        {#each listOfCatergories as eachCatergory}
          <li><a href="/" class="flex space-x-1.5 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-700 rounded-lg ">
            <img src="/logos/github.svg" alt="icon" class="w-7">
            <span class="">{eachCatergory}</span>
          </a></li>
        {/each}
      </ul>
    </section>

    <section class="w-full flex flex-col items-center justify-center p-2 text-sm">
      <a href="/" class="hover:underline "><p class="">&copy; 2023 CheapAli</p></a>
    </section>
  </aside>
  
  <main class="h-full w-full space-y-8 md:space-y-4">
    <div class="w-full h-44 bg-neutral-100 dark:bg-neutral-900 rounded-lg overflow-hidden shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20">
      <img src="/images/banner.jpg" alt="CheapAli'sbanner" class="w-full h-full object-cover">
    </div>

    <section class="w-full h-full bg-neutral-100 dark:bg-neutral-900 md:p-4 rounded-lg overflow-y-auto">
      <h3 class="font-medium text-lg">Featured Products</h3>

      <section class="w-full grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 py-4">
        {#each listOfItems as eachItem}
          <ItemCard name={eachItem.name} newPrice={eachItem.newPrice} oldPrice={eachItem.oldPrice} imgSrc={eachItem.imgSrc}/>
        {/each}
      </section>
    </section>
  </main>
</section>

<footer class="w-full md:h-96 bg-neutral-200 dark:bg-neutral-800 px-4 md:p-2 flex">
  <div class="md:w-10/12 md:mx-auto flex flex-col md:flex-row md:justify-around py-4 space-y-10 md:space-y-0">
    <section class="w-full md:w-3/12 flex md:flex-col items-center justify-between md:items-start md:justify-normal space-y-">
      <a href="/" class="">
        <div class="">
          <img src="/images/cheapali-logo.png" alt="" class="w-28">
        </div>
      </a>
      
      <div class="">
        <div class="">
          <a href="tel:+2340123456789" class=" hover:underline">
            <!-- <i class="icon icon-"></i> -->
            <span class="">+234 012 345 6789</span>
          </a>
        </div>
        <div class="">
          <a href="mailto:shop@gmail.com" class=" hover:underline">
            <!-- <i class="icon icon-"></i> -->
            <span class="">shop@gmail.com</span>
          </a>
        </div>
      </div>
    </section>
    <section class="w-full md:w-5/12 bg-rose500 flex flex-col md:flex-row space-y-7 md:space-y-0 md:space-x-14">
      <ul class="space-y-2">
        <li class="font-semibold">Website</li>
        <li class=""><a href="/" class="hover:underline ">Search</a></li>
        <li class=""><a href="/" class="hover:underline ">Condition Guide</a></li>
        <li class=""><a href="/" class="hover:underline ">About Rip & Ship</a></li>
      </ul>
      <ul class="space-y-2">
        <li class="font-semibold">Our Company</li>
        <li class=""><a href="/" class="hover:underline ">Refund Policy</a></li>
        <li class=""><a href="/" class="hover:underline ">Privacy Policy</a></li>
        <li class=""><a href="/" class="hover:underline ">Shipping Policy</a></li>
        <li class=""><a href="/" class="hover:underline ">Contact Information</a></li>
        <li class=""><a href="/" class="hover:underline ">Terms of Service</a></li>
      </ul>
    </section>
    <section class="w-full md:w-4/12 space-y-3">
      <div class="-space-y-0.5">
        <h3 class="font-medium text-lg">Newsletter</h3>
        <p class="">Suscribe to our newsletter</p>
      </div>
      <div class="space-y-2">
        <input type="email" name="newsletterEmail" id="newsletterEmail" placeholder="Enter your email" class="w-full bg-neutral-900 dark:bg-neutral-100 text-neutral-100 dark:text-neutral-900 border-none rounded-md p-2 placeholder-neutral-500">
        <button class="w-full p-2 rounded-lg bg-amber-600 hover:bg-amber-700 font-medium">Submit</button>
      </div>
    </section>
  </div>
</footer>