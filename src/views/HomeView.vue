<template>
  <section class="px-5 pt-5">
    <h4 class="font-semibold">Product Categories</h4>
    <p>Valvindo provide a complete range of quality products serving the nation businesses major industries
        for over three decades. Pipeline products stockist and distributor carrying a wide range of valves,
        flanges, fittings, pipes, gaskets and accessories to meet your every needs.
    </p>

    <!-- Category -->
    <div v-for="cat in product_list" :key="cat.id">
      <h4 class="font-semibold mt-4 mb-2">{{ cat.category }}</h4>

      <div class="grid grid-cols-6 gap-1">
        <div class="border-2 rounded-md px-2 py-2 flex items-end justify-between" v-for="product in cat.products" :key="product.id">
          <span class="inline-block">{{ product.name }}</span>
          <img :src="product.images" class="h-20">
        </div>
      </div>
    </div>
    
  </section>
  
  <section class="px-5 pt-10">
    <h1 class="text-center text-xl font-bold text-red-500">Vision <span class="text-[#002062]">&</span> Mission</h1>
    <div class="flex items-center justify-center mt-1">
      <div class="w-1.5 h-1.5 bg-red-500 rounded-full"></div>
      <div class="h-0.5 w-24 bg-red-500"></div>
      <div class="w-1.5 h-1.5 bg-red-500 rounded-full"></div>
    </div>

    <div class="grid grid-cols-3 gap-2 mx-24 my-20">
      <div class="bg-[#002062] h-60 relative text-white p-10">
        <div class="w-16 h-16 bg-[#EB1F29] rounded-full absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2"></div>
        <h1 class="text-center text-xl font-bold mb-3">Customer</h1>
        <p class="text-center">Focus on customer needs to provide one stop solutions for customers through wide range of high quality products coupled with good availability and fast delivery time</p>
      </div>

      <div class="bg-[#002062] h-60 relative text-white p-10">
        <div class="w-16 h-16 bg-[#EB1F29] rounded-full absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2"></div>
        <h1 class="text-center text-xl font-bold mb-3">Products</h1>
        <p class="text-center">Leading the industry through partnership with top brands in every product categories</p>
      </div>

      <div class="bg-[#002062] h-60 relative text-white p-10">
        <div class="w-16 h-16 bg-[#EB1F29] rounded-full absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2"></div>
        <h1 class="text-center text-xl font-bold mb-3">People</h1>
        <p class="text-center">Continuous investments in our human resources and systems to provide best services for our customers' needs</p>
      </div>
    </div>
  </section>
</template>

<script>
  import axios from 'axios'

export default {
  name: 'HomeView',
  data () {
    return {
      product_list: [],
    }
  },
  mounted () {
    this.getProduct()
  },
  methods:{
    async getProduct(){
      await axios.get('http://localhost:8000/product/')
      .then((res) => {
        console.log(res.data);
        this.product_list = res.data
      })
      .catch(error =>
        this.errors = error.response.data.message
      );
    },
  }
}
</script>
