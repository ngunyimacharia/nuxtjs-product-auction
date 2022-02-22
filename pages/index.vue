<template>
<div class="bg-white">
  <div class="pt-6">
    <!-- Image gallery -->
    <div class="mt-6 max-w-2xl mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:grid lg:grid-cols-3 lg:gap-x-8">
      <div class="hidden aspect-w-3 aspect-h-4 rounded-lg overflow-hidden lg:block">
        <img src="https://tailwindui.com/img/ecommerce-images/product-page-02-secondary-product-shot.jpg" alt="Two each of gray, white, and black shirts laying flat." class="w-full h-full object-center object-cover">
      </div>
      <div class="hidden lg:grid lg:grid-cols-1 lg:gap-y-8">
        <div class="aspect-w-3 aspect-h-2 rounded-lg overflow-hidden">
          <img src="https://tailwindui.com/img/ecommerce-images/product-page-02-tertiary-product-shot-01.jpg" alt="Model wearing plain black basic tee." class="w-full h-full object-center object-cover">
        </div>
        <div class="aspect-w-3 aspect-h-2 rounded-lg overflow-hidden">
          <img src="https://tailwindui.com/img/ecommerce-images/product-page-02-tertiary-product-shot-02.jpg" alt="Model wearing plain gray basic tee." class="w-full h-full object-center object-cover">
        </div>
      </div>
      <div class="aspect-w-4 aspect-h-5 sm:rounded-lg sm:overflow-hidden lg:aspect-w-3 lg:aspect-h-4">
        <img src="https://tailwindui.com/img/ecommerce-images/product-page-02-featured-product-shot.jpg" alt="Model wearing plain white basic tee." class="w-full h-full object-center object-cover">
      </div>
    </div>

    <!-- Product info -->
    <div class="max-w-2xl mx-auto pt-10 pb-16 px-4 sm:px-6 lg:max-w-7xl lg:pt-16 lg:pb-24 lg:px-8 lg:grid lg:grid-cols-3 lg:grid-rows-[auto,auto,1fr] lg:gap-x-8">
      <div class="lg:col-span-2 lg:border-r lg:border-gray-200 lg:pr-8">
        <h1 class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl">Basic Tee 6-Pack</h1>
      </div>

      <!-- Bids -->
      <div class="mt-4 lg:mt-0 lg:row-span-3">
          <ul role="list" class="divide-y divide-gray-200">
            <li class="py-4">
              <div class="flex space-x-3">
                <img class="h-6 w-6 rounded-full" src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=3&w=256&h=256&q=80" alt="">
                <div class="flex-1 space-y-1">
                  <div class="flex items-center justify-between">
                    <h3 class="text-sm font-medium">Lindsay Walton</h3>
                    <p class="text-sm text-gray-500">1h</p>
                  </div>
                  <p class="text-sm text-gray-500">Deployed Workcation (2d89f0c8 in master) to production</p>
                </div>
              </div>
            </li>

            <!-- More items... -->
          </ul>

      </div>

      <div class="py-10 lg:pt-6 lg:pb-16 lg:col-start-1 lg:col-span-2 lg:border-r lg:border-gray-200 lg:pr-8">
        <!-- Description and details -->
        <div>
          <h3 class="sr-only">Description</h3>

          <div class="space-y-6">
            <p class="text-base text-gray-900">The Basic Tee 6-Pack allows you to fully express your vibrant personality with three grayscale options. Feeling adventurous? Put on a heather gray tee. Want to be a trendsetter? Try our exclusive colorway: &quot;Black&quot;. Need to add an extra pop of color to your outfit? Our white tee has you covered.</p>
          </div>
        </div>

        <div class="mt-10">
          <h3 class="text-sm font-medium text-gray-900">Highlights</h3>

          <div class="mt-4">
            <ul role="list" class="pl-4 list-disc text-sm space-y-2">
              <li class="text-gray-400"><span class="text-gray-600">Hand cut and sewn locally</span></li>

              <li class="text-gray-400"><span class="text-gray-600">Dyed with our proprietary colors</span></li>

              <li class="text-gray-400"><span class="text-gray-600">Pre-washed &amp; pre-shrunk</span></li>

              <li class="text-gray-400"><span class="text-gray-600">Ultra-soft 100% cotton</span></li>
            </ul>
          </div>
        </div>

        <div class="mt-10">
          <h2 class="text-sm font-medium text-gray-900">Details</h2>

          <div class="mt-4 space-y-6">
            <p class="text-sm text-gray-600">The 6-Pack includes two black, two white, and two heather gray Basic Tees. Sign up for our subscription service and be the first to get new, exciting colors, like our upcoming &quot;Charcoal Gray&quot; limited release.</p>
          </div>

          <div>
            Video by Ylanite Koppens from Pexels
            Video by Ashutosh Sonwani from Pexels
            Photo by Juan C. Palacios from Pexels
            Photo by Skylar Kang from Pexels
            Photo by Mark Stebnicki from Pexels
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
