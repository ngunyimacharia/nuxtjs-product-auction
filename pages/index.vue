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
          <ul v-if="winningBid" role="list" class="divide-y divide-gray-200">
            <li class="py-4">
              <div class="flex space-x-3">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
                </svg>
                <div class="flex-1 space-y-1">
                  <div class="flex items-center justify-between">
                    <h3 class="text-sm font-medium">{{winningBid.name}}</h3>
                    <p class="text-sm text-gray-500">$ {{new Intl.NumberFormat().format(winningBid.amount)}}</p>
                  </div>
                  <p class="text-sm text-gray-500">
                    {{
                      (new Date(winningBid.created_at)).toLocaleString("en-US")
                    }}
                  </p>
                </div>
              </div>
            </li>
          </ul>

          <div class="py-5 pb-10">
            <div class="sm:mx-auto sm:w-full sm:max-w-md">
              <div class="bg-white py-8 px-4 shadow sm:rounded-lg sm:px-10">
                <form class="space-y-6" @submit.prevent="sendBid">
                  <div>
                    <label for="name" class="block text-sm font-medium text-gray-700"> Names </label>
                    <div class="mt-1">
                      <input 
                        id="name" 
                        name="name" 
                        type="text" 
                        v-model="newBid.name"
                        required 
                        class="appearance-none block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
                      />
                    </div>
                  </div>

                  <div>
                    <label for="amount" class="block text-sm font-medium text-gray-700"> Amount </label>
                    <div class="mt-1">
                      <input 
                        id="amount" 
                        name="amount" 
                        type="number" 
                        v-model="newBid.amount"
                        required 
                        class="appearance-none block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
                      />
                    </div>
                  </div>

                  <div>
                    <button 
                      type="submit" 
                      class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
                    >Place Bid</button>
                  </div>
                </form>

              </div>
            </div>
          </div>

          <p v-if="!bids">Loading bids...</p>
          <ul v-else role="list" class="divide-y divide-gray-200">
            <li v-for="bid in bids" :key="bid.id" class="py-4">
              <div class="flex space-x-3">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-yellow-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
                <div class="flex-1 space-y-1">
                  <div class="flex items-center justify-between">
                    <h3 class="text-sm font-medium">{{bid.name}}</h3>
                    <p class="text-sm text-gray-500">$ {{new Intl.NumberFormat().format(bid.amount)}}</p>
                  </div>
                  <p class="text-sm text-gray-500">
                    {{
                      (new Date(bid.created_at)).toLocaleString("en-US")
                    }}
                  </p>
                </div>
              </div>
            </li>
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

import { createClient } from '@supabase/supabase-js'

export default {
  data(){
    return {
      gallery:null,
      supabase:null,
      winningBid:null,
      bids:null,
      newBid:{
        name:null,
        amount:null
      }
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

    this.supabase = createClient(process.env.NUXT_ENV_SUPABASE_URL, process.env.NUXT_ENV_SUPABASE_KEY);

    this.loadBids();

    this.listenToBids();
  },

  beforeDestroy(){
    console.log("Removing");
    this.supabase.removeAllSubscriptions();
  },

  methods:{

    async loadBids(){
      this.loadWinningBid();

      const resp = await this.supabase
        .from('bids')
        .select()
        .order('id', { ascending: false });

      if(resp.status != 200){
        console.log(resp);
      }

      this.bids = resp.data;
    },

    async loadWinningBid(){
      const resp = await this.supabase
        .from('bids')
        .select()
        .order('amount', { ascending: false }) 
        .limit(1)
        .single();

      if(resp.status != 200){
        console.log(resp);
      }

      this.winningBid = resp.data;
    },

    listenToBids(){
      const subscription = this.supabase
      .from('bids')
      .on('*', () => {
        this.loadBids();
      })
      .subscribe()
    },

    async sendBid(){
      const resp = await this.supabase
        .from('bids')
        .insert([
          this.newBid
        ]);

      if(resp.status != 201){
            console.log(resp);
      }

      this.newBid = {
        name:null,
        amount:null
      };
    },
  }
}
</script>
