<script>
  import ItemCard from "$lib/components/ItemCard.svelte";
  import { scale, slide } from "svelte/transition";

  const listOfCatergories = [
    {
      name: "Gadgets and Electronics",
      icon: "mdi-signal-5g",
      color: "text-emerald-500",
      url: "/",
    },
    {
      name: "Laptop accessories",
      icon: "mdi-laptop",
      color: "text-violet-500",
      url: "/",
    },
    {
      name: "Phone accessories",
      icon: "mdi-cellphone",
      color: "text-cyan-500",
      url: "/",
    },
    {
      name: "Gaming accessories",
      icon: "mdi-cradle",
      color: "text-lime-500",
      url: "/",
    },
    {
      name: "Place an Aliexpress order",
      icon: "mdi-cash",
      color: "text-amber-500",
      url: "/",
    },
  ]
  const listOfProducts = [
    {
      name: "Watches",
      icon: "mdi-watch",
      color: "text-rose-500",
      url: "/",
    },
    {
      name: "Phones",
      icon: "mdi-phone",
      color: "text-blue-500",
      url: "/",
    },
    {
      name: "Glasses",
      icon: "mdi-glasses",
      color: "text-amber-500",
      url: "/",
    },
    {
      name: "Camera",
      icon: "mdi-camera",
      color: "text-purple-500",
      url: "/",
    },
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

<nav class="w-full py-2 px-4 flex items-center justify-between bg-neutral-100 dark:bg-neutral-800">
  <a href="/" class="">
    <div class="">
      <img src="/images/cheapali-logo.png" alt="" class="w-14">
    </div>
  </a>
  
  <section class="flex items-center space-x-4">
    <div class="flex items-center space-x-2 rounded-full border-2 border-transparent dark:bg-neutral-700 bg-neutral-300 focus-within:border-amber-600">
      <!-- <i class="pl-3 pr-1.5">Q</i> -->
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 ml-2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
      </svg>      
      <input type="text" name="searchInput" id="searchInput" placeholder="Search CheapAli" class="w-full bg-transparent bborder-none focus:border-none focus:outline-0 focus:ring-0 rounded-r-full py-2 pr-2 text-sm">
      <!-- <button class="p-2 rounded-lg bg-amber-600 hover:bg-amber-700 font-medium">Q</button> -->
    </div>

    <section class="flex">
      <button on:click={handleNavBarMenuDrawer} class="flex p-1.5 bg-neutral-200 hover:bg-neutral-300 dark:bg-neutral-800 dark:hover:bg-neutral-700 rounded-md">
        <svg transition:scale xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
      
      {#if isNavBarMenuDrawer}
        <div class="w-full h-full fixed top-0 right-0 z-20">
          <div on:click={handleNavBarMenuDrawer} class="w-full h-full absolute bg-transparent/80"/>

          <section transition:slide={{axis: 'x'}} class="fixed top-0 right-0 z-40 h-full w-11/12 md:w-96  rounded-l-lg bg-neutral-100 dark:bg-neutral-900 pt-4 pb-1 px-4 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-900/20 space-y-2">
            <div class="flex items-center justify-between">
              <h3 class="font-medium text-lg">CheapAli</h3>

              <button on:click={handleNavBarMenuDrawer} class="flex p-1.5 bg-neutral-200 hover:bg-neutral-300 dark:bg-neutral-800 dark:hover:bg-neutral-700 rounded-md">
                <svg transition:scale xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 rotate-45">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                </svg>                
              </button>
            </div>
            <div class="w-full flex flex-col justify-between space-y-20">
              <ul class="w-full space-y-1">
                <li><a href="/" class="flex space-x-3 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-800 rounded-lg ">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                  </svg>                
                  <span class="font-medium">0</span>
                </a></li>
                <li><a href="/" class="flex space-x-3 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-800 rounded-lg ">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
                  </svg>                  
                  <span class="">Home</span>
                </a></li>
                <li><a href="/" class="flex space-x-3 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-800 rounded-lg ">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
                  </svg>
                  <span class="">Contact</span>
                </a></li>
                <li><a href="/" class="flex space-x-3 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-800 rounded-lg ">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M11.25 11.25l.041-.02a.75.75 0 011.063.852l-.708 2.836a.75.75 0 001.063.853l.041-.021M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-9-3.75h.008v.008H12V8.25z" />
                  </svg>                  
                  <span class="">About</span>
                </a></li>
              </ul>
              
              <ul>
                <li><a href="/" class="flex space-x-3 items-center justify-center px-3 py-1.5 bg-amber-600 hover:bg-amber-700 text-neutral-900 rounded-lg font-medium">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15M12 9l-3 3m0 0l3 3m-3-3h12.75" />
                  </svg>
                  <span class="">Login</span>
                </a></li>
              </ul>
            </div>
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
          <li><a href="{eachProduct.url}" class="flex space-x-2 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-700 rounded-lg ">
            {#if eachProduct.icon !== ""}
              <!-- content here -->
              <i class="mdi {eachProduct.icon} text-xl {eachProduct.color}"></i>
            {:else}
              <!-- else content here -->
              <i class="mdi mdi-inbox-outline text-xl"></i>
            {/if}
            <span class="">{eachProduct.name}</span>
          </a></li>
        {/each}
      </ul>
    </section>
    
    <section class="w-full rounded-lg bg-neutral-100 dark:bg-neutral-800 pt-4 pb-1 px-1 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20 space-y-2">
      <h3 class="font-medium text-lg px-3">Categories</h3>
      <ul class="w-full space-y-1">
        {#each listOfCatergories as eachCatergory}
        <li><a href="{eachCatergory.url}" class="flex space-x-2 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-700 rounded-lg ">
          {#if eachCatergory.icon !== ""}
            <!-- content here -->
            <i class="mdi {eachCatergory.icon} text-xl {eachCatergory.color}"></i>
          {:else}
            <!-- else content here -->
            <i class="mdi mdi-cards-outline text-xl"></i>
          {/if}
          <span class="">{eachCatergory.name}</span>
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