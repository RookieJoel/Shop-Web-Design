<script lang="ts">
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import StatItem from "./components/StatItem.svelte";
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

    <section class="mt-3">
      <img src="https://placehold.co/500x500" alt="Fashion preview" class="rounded-xl" />
    </section>
  </div>
</div>

<div class="bg-gray-800 text-center text-white py-4">
 <h2 class="font-bold text-3xl">New Arrivals</h2>
</div>




