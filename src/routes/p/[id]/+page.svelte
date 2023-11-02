<script>
  const product = {
    name: "iPhone 15 leather case",
    newPrice: "$179.99",
    oldPrice: "$279.99",
    imgSrc: "/images/iphone-15-case.jpg",
    url: "81hen192e",
  }
</script>

<section class="w-full min-h-screen">
  <section class="w-full lg:w-10/12 lg:mx-auto h-full p-10 flex space-x-10">
    <section class="w-6/12 h-96 bg-rose-500 rounded-xl overflow-hidden">
      <img src="{product.imgSrc}" alt="{product.name}" class="w-full h-full object-cover">
    </section>

    <section class="w-6/12 h-full py-5 space-y-2">
      <h3 class="font-medium text-2xl">{product.name}</h3>
      <h4 class="font-medium text-3xl">{product.newPrice}</h4>
      <h4 class="line-through text-lg text-rose-500">{product.oldPrice}</h4>
    </section>
  </section>
</section>