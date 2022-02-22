<template>
<div class="bg-white">
  <div class="pt-6">

    <!-- Cloudinary product gallery -->
      <div 
        id="my-gallery"

      ></div>

    <!-- Product info -->
    <div class="max-w-2xl mx-auto pt-10 pb-16 px-4 sm:px-6 lg:max-w-7xl lg:pt-16 lg:pb-24 lg:px-8 lg:grid lg:grid-cols-3 lg:grid-rows-[auto,auto,1fr] lg:gap-x-8">
      <div class="lg:col-span-2 lg:border-r lg:border-gray-200 lg:pr-8">
        <h1 class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl">New Zealand Apple Orchid for Sale</h1>
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
            <p class="text-base text-gray-900">
              The property is set up with a strong solar borehole with water bottling facilities and reverse osmosis purification.
            </p>
            <p class="text-base text-gray-900">
              The property also has around 1500m² of shade net tunnels – perfect for growing a variety of plants in ideal conditions. An additional 1000m² of infrastructure is installed to expand the shade netting cover further.
            </p>
            <p class="text-base text-gray-900">
              A rustic 1-bedroom, open plan house and staff quarters make up the dwellings on offer.
            </p>
            <p class="text-base text-gray-900">
              An additional 200m² building consists of 2 rooms with points for extractor fans, ample power connections, and 3 Air conditioners per room making this an ideal place for growing plants in refined and controlled conditions or keeping produce as fresh as possible for long periods in storage. A 3rd room is in the form of a walk-in fridge/freezer.
            </p>
          </div>
        </div>

        <div class="mt-10">
          <h3 class="text-sm font-medium text-gray-900">Photo credits</h3>

          <div class="mt-4">
            <ul role="list" class="pl-4 list-disc text-sm space-y-2">
              <li class="text-gray-400">
                <span class="text-gray-600">
                  Video by Ylanite Koppens from Pexels
                </span>
              </li>
              <li class="text-gray-400">
                <span class="text-gray-600">
                  Video by Ashutosh Sonwani from Pexels
                </span>
              </li>
              <li class="text-gray-400">
                <span class="text-gray-600">
                  Photo by Juan C. Palacios from Pexels
                </span>
              </li>
              <li class="text-gray-400">
                <span class="text-gray-600">
                  Photo by Skylar Kang from Pexels
                </span>
              </li>
              <li class="text-gray-400">
                <span class="text-gray-600">
                  Photo by Mark Stebnicki from Pexels
                </span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
export default {
  data(){
    return {
      gallery:null
    }
  },
  mounted(){
    this.gallery = cloudinary.galleryWidget({ 
      container: "#my-gallery", 
      cloudName: process.env.NUXT_ENV_CLOUDINARY_CLOUD_NAME, 
      aspectRatio: "16:9",
      mediaAssets: [
        { tag: "npa-apple", },
        { tag: "npa-apple", mediaType: "video" },
      ] ,
      videoProps: { playerType: "cloudinary" }  
    });

    this.gallery.render();

    console.log("gallery",this.gallery);
  }
}
</script>
