<script>
  import ItemCard from "$lib/components/ItemCard.svelte";
  import ThemeBtn from "$lib/components/ThemeBtn.svelte";
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

<section class="w-full h-full lg:h-screen md:flex relative">
  <aside class="hidden lg:block h-full w-3/12 stickytop-0 space-y-7 bg-neutral-100 dark:bg-neutral-800 p-7">
    <h1 class="font-semibold text-lg">CheapAli</h1>

    <section class="space-y-10">
      <section class="w-full space-y-1">
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6A2.25 2.25 0 016 3.75h2.25A2.25 2.25 0 0110.5 6v2.25a2.25 2.25 0 01-2.25 2.25H6a2.25 2.25 0 01-2.25-2.25V6zM3.75 15.75A2.25 2.25 0 016 13.5h2.25a2.25 2.25 0 012.25 2.25V18a2.25 2.25 0 01-2.25 2.25H6A2.25 2.25 0 013.75 18v-2.25zM13.5 6a2.25 2.25 0 012.25-2.25H18A2.25 2.25 0 0120.25 6v2.25A2.25 2.25 0 0118 10.5h-2.25a2.25 2.25 0 01-2.25-2.25V6zM13.5 15.75a2.25 2.25 0 012.25-2.25H18a2.25 2.25 0 012.25 2.25V18A2.25 2.25 0 0118 20.25h-2.25A2.25 2.25 0 0113.5 18v-2.25z" />
            </svg>                      
            <span class="">Dashboard</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M16.5 6v.75m0 3v.75m0 3v.75m0 3V18m-9-5.25h5.25M7.5 15h3M3.375 5.25c-.621 0-1.125.504-1.125 1.125v3.026a2.999 2.999 0 010 5.198v3.026c0 .621.504 1.125 1.125 1.125h17.25c.621 0 1.125-.504 1.125-1.125v-3.026a2.999 2.999 0 010-5.198V6.375c0-.621-.504-1.125-1.125-1.125H3.375z" />
            </svg>            
            <span>Active Bids</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
            </svg>            
            <span>Market</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
            </svg>
            
            <span>Favourites</span>
          </div>
        </a>
      </section>

      <hr class="border-neutral-300 dark:border-neutral-700">

      <section class="w-full space-y-1">
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M15.182 15.182a4.5 4.5 0 01-6.364 0M21 12a9 9 0 11-18 0 9 9 0 0118 0zM9.75 9.75c0 .414-.168.75-.375.75S9 10.164 9 9.75 9.168 9 9.375 9s.375.336.375.75zm-.375 0h.008v.015h-.008V9.75zm5.625 0c0 .414-.168.75-.375.75s-.375-.336-.375-.75.168-.75.375-.75.375.336.375.75zm-.375 0h.008v.015h-.008V9.75z" />
            </svg>            
            <span>My Portfolio</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M20.25 6.375c0 2.278-3.694 4.125-8.25 4.125S3.75 8.653 3.75 6.375m16.5 0c0-2.278-3.694-4.125-8.25-4.125S3.75 4.097 3.75 6.375m16.5 0v11.25c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125V6.375m16.5 0v3.75m-16.5-3.75v3.75m16.5 0v3.75C20.25 16.153 16.556 18 12 18s-8.25-1.847-8.25-4.125v-3.75m16.5 0c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125" />
            </svg>            
            <span>History</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v12m-3-2.818l.879.659c1.171.879 3.07.879 4.242 0 1.172-.879 1.172-2.303 0-3.182C13.536 12.219 12.768 12 12 12c-.725 0-1.45-.22-2.003-.659-1.106-.879-1.106-2.303 0-3.182s2.9-.879 4.006 0l.415.33M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>            
            <span>Wallet</span>
          </div>
        </a>
        <a href="/" class="w-full focus:outline-none focus:ring-1 focus:ring-amber-500 flex rounded-lg">
          <div class="w-full px-2 py-1.5 rounded-lg hover:bg-neutral-300 flex items-center space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9.594 3.94c.09-.542.56-.94 1.11-.94h2.593c.55 0 1.02.398 1.11.94l.213 1.281c.063.374.313.686.645.87.074.04.147.083.22.127.324.196.72.257 1.075.124l1.217-.456a1.125 1.125 0 011.37.49l1.296 2.247a1.125 1.125 0 01-.26 1.431l-1.003.827c-.293.24-.438.613-.431.992a6.759 6.759 0 010 .255c-.007.378.138.75.43.99l1.005.828c.424.35.534.954.26 1.43l-1.298 2.247a1.125 1.125 0 01-1.369.491l-1.217-.456c-.355-.133-.75-.072-1.076.124a6.57 6.57 0 01-.22.128c-.331.183-.581.495-.644.869l-.213 1.28c-.09.543-.56.941-1.11.941h-2.594c-.55 0-1.02-.398-1.11-.94l-.213-1.281c-.062-.374-.312-.686-.644-.87a6.52 6.52 0 01-.22-.127c-.325-.196-.72-.257-1.076-.124l-1.217.456a1.125 1.125 0 01-1.369-.49l-1.297-2.247a1.125 1.125 0 01.26-1.431l1.004-.827c.292-.24.437-.613.43-.992a6.932 6.932 0 010-.255c.007-.378-.138-.75-.43-.99l-1.004-.828a1.125 1.125 0 01-.26-1.43l1.297-2.247a1.125 1.125 0 011.37-.491l1.216.456c.356.133.751.072 1.076-.124.072-.044.146-.087.22-.128.332-.183.582-.495.644-.869l.214-1.281z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>            
            <span>Settings</span>
          </div>
        </a>
      </section>
    </section>
  </aside>
  
  <section class="h-full w-full flex flex-col overflow-y-auto">
    <nav class="w-full lg:w-11/12 lg:mx-auto p-7 flex items-center justify-between space-x-7">
      <section class="w-8/12">
        <div class="w-full rounded-full bg-neutral-100 dark:bg-neutral-800 flex items-center focus-within:ring-2 focus-within:ring-amber-500">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 mx-2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
          </svg>
          <input type="text" class="w-full py-2 pl-1 pr-2 bg-transparent focus:outline-none focus:ring-0" placeholder="Search any product">
        </div>
      </section>

      <section class="flex items-center space-x-4">
        <div class="rounded-full flex">
          <ThemeBtn bg={"bg-neutral-100 hover:bg-neutral-200 dark:bg-neutral-800 dark:hover:bg-neutral-700"}/>
        </div>
  
        <div class="rounded-full flex p-1 bg-neutral-100 hover:bg-neutral-200 dark:bg-neutral-800 dark:hover:bg-neutral-700">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
          </svg>        
        </div>
  
        <div class="rounded-full flex items-center p-1 bg-neutral-100 hover:bg-neutral-200 dark:bg-neutral-800 dark:hover:bg-neutral-700 space-x-1">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
          </svg>
          
          <span class="pr-1">@bnierimi</span>
        </div>
      </section>
    </nav>

    <section class="w-full lg:w-11/12 lg:mx-auto h- flex space-x-7 p-7">
      <section class="w-full h-">
        <main class="w-full h- space-y-6">
          <div class="w-full h-44 bg-neutral-100 dark:bg-neutral-900 rounded-lg overflow-hidden shadow-lg shadow-neutral-400/20 dark:shadow-neutral-800/20">
            <img src="/images/banner.jpg" alt="CheapAli'sbanner" class="w-full h-full object-cover">
          </div>

          <section class="w-full h- bg-neutral100 dark:bg-neutral900 md:p-4 rounded-lg">
            <h3 class="font-medium text-xl">Featured Products</h3>
      
            <section class="w-full grid grid-cols-2 md:grid-cols-3 lg:grid-cols- gap-5 py-4">
              {#each listOfItems as eachItem}
                <ItemCard name={eachItem.name} newPrice={eachItem.newPrice} oldPrice={eachItem.oldPrice} imgSrc={eachItem.imgSrc} url={eachItem.url}/>
              {/each}
            </section>
          </section>
        </main>
      </section>

      <!-- <section class="w-4/12 h-full space-y-4 flex flex-col">
        <section class="bg-neutral-100 w-full h-96 rounded-xl"></section>
        <section class="bg-neutral-100 w-full h-full rounded-xl"></section>
      </section> -->
    </section>

    <footer class="w-full h-96 bg-neutral-200 dark:bg-neutral-800 px-4 md:p-2 flex py-10">
      <div class="md:w-10/12 md:mx-auto flex flex-col md:flex-row md:justify-around py-4 space-y-7 md:space-y-0">
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
  </section>
</section>