<script lang="ts">
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import StatItem from "./components/StatItem.svelte";
  import Card from "./components/Card.svelte";
  const stats = [
    { count: '1100+', label: 'Happy Customers' },
    { count: '800+', label: 'Projects Completed' },
    { count: '1000+', label: 'Positive Reviews' },
  ];

</script>

<Header />
<Nav />

<div class="w-full bg-neutral-300">
  <div class="container mx-auto flex flex-wrap items-center justify-between px-4 py-8">
    
    <section class="mt-3 max-w-xl">
      <h1 class="font-extrabold text-6xl">Find clothes that matches your style!</h1>
      <p class="pt-5">
        Discover curated collections tailored to your personality, mood, and lifestyle. From everyday essentials to bold statement pieces, we've got everything you need to express yourself confidently.
      </p>
      <a href="#" class="bg-blue-950 text-center text-white px-10 py-2.5 mt-5 rounded-full inline-block">
        Shop Now
      </a>
      
      <section>
        <ul class="inline-flex gap-8 pt-4">
          {#each stats as stat}
            <StatItem count={stat.count} label={stat.label} />
          {/each}
        </ul>
      </section>
    </section>


    <section class="mt-3 mr-3">
      <img src="https://placehold.co/800x500" alt="Fashion preview" class="rounded-xl" />
    </section>
  </div>
</div>

<div class="bg-gray-800 text-center text-white py-4">
 <h2 class="font-bold text-3xl">New Arrivals</h2>
</div>

<section class="container mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-4">
  <Card ImgSrc="https://placehold.co/350x300" text="Stylish Jacket" rating={4.5} size={24} price={49.99} />
  <Card ImgSrc="https://placehold.co/350x300" text="Casual Sneakers" rating={4.0} size={24} price={59.99} />
  <Card ImgSrc="https://placehold.co/350x300" text="Elegant Dress" rating={5.0} size={24} price={79.99} />
  <Card ImgSrc="https://placehold.co/350x300" text="Trendy Backpack" rating={4.2} size={24} price={39.99} />
  <div class="col-span-full flex justify-center">
    <button class="bg-blue-950 text-white px-4 py-3 rounded-lg hover:bg-blue-800 transition duration-300">
      View All Products
    </button>
  </div>
</section>

<section>
  <div class="container mx-auto">
    <div class="bg-gray-200 text-center py-8 rounded-3xl">
      <h2 class="text-3xl font-bold mb-4">Find Your Fit</h2>
      <h3 class="text-xl mb-6 font-bold">Flaunt Your Style</h3>
      <div class="grid grid-cols-4 grid-rows-2 gap-4 p-3">

        <div class="style-item col-span-2 bg-[url('https://placehold.co/600x300')]">
          <h4 class="text-xl font-semibold mb-2">Casual Wear</h4>
        </div>

        <div class="style-item row-span-2 bg-[url('https://placehold.co/300x600')]">
          <h4 class="text-xl font-semibold mb-2">Formal Wear</h4>
        </div>

        <div class="style-item row-span-2 bg-[url('https://placehold.co/300x600')]">
          <h4 class="text-xl font-semibold mb-2">Sportswear</h4>
        </div>
        
        <div class="style-item bg-[url('https://placehold.co/300x250')]">
          <h4 class="text-xl font-semibold mb-2">Accessories</h4>
          <img src="https://placehold.co/300x250" alt="Accessories" class="rounded-lg mt-2">
        </div>

        <div class="style-item bg-[url('https://placehold.co/300x250')]">
          <h4 class="text-xl font-semibold mb-2">Footwear</h4>
          <img src="https://placehold.co/300x250" alt="Footwear" class="rounded-lg mt-2">
        </div>

    </div>
  </div>
</section>

