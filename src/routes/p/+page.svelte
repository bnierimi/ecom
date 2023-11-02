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
    },
    {
      name: "Phones",
      icon: "mdi-phone",
      color: "text-blue-500",
    },
    {
      name: "Glasses",
      icon: "mdi-glasses",
      color: "text-amber-500",
    },
    {
      name: "Camera",
      icon: "mdi-camera",
      color: "text-purple-500",
    },
  ]
  const listOfItems = [
    {
      name: "iPhone 15 leather case",
      newPrice: "$179.99",
      oldPrice: "$279.99",
      imgSrc: "/images/iphone-15-case.jpg",
      url: "81hen192e",
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
      imgSrc: "/images/watch1.jpg",
      url: "d289ghb32",
    },
    {
      name: "iPhone 11 case",
      newPrice: "$99.99",
      oldPrice: "$109.99",
      imgSrc: "/images/iphone-11-case.jpg",
      url: "f28gf92ew",
    },
    {
      name: "Men's Package watch",
      newPrice: "$19.99",
      oldPrice: "$79.99",
      imgSrc: "/images/watch4.jpg",
      url: "28dh23e27",
    },
    {
      name: "Samsung S20 case",
      newPrice: "$19.99",
      oldPrice: "$79.99",
      imgSrc: "/images/samsung-s20-case.jpg",
      url: "nf92h4r23",
    },
  ]
</script>

<section class="w-full h-full p-4 md:flex md:space-x-4 relative">
  <aside class="hidden lg:block h-full  w-3/12 sticky top-4 space-y-4">
    <section class="w-full rounded-lg bg-neutral-100 dark:bg-neutral-800 pt-4 pb-1 px-1 shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20 space-y-2">
      <h3 class="font-medium text-lg px-3">Products</h3>
      <ul class="w-full space-y-1">
        {#each listOfProducts as eachProduct}
          <li><a href="/" class="flex space-x-2 items-center px-3 py-1.5 hover:bg-transparent/10 dark:hover:bg-neutral-700 rounded-lg ">
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
          <ItemCard name={eachItem.name} newPrice={eachItem.newPrice} oldPrice={eachItem.oldPrice} imgSrc={eachItem.imgSrc} url={eachItem.url}/>
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