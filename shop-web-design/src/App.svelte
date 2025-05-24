<script lang="ts">
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import StatItem from "./components/StatItem.svelte";
  
  const stats = [
    { count: '1100+', label: 'Happy Customers' },
    { count: '800+', label: 'Projects Completed' },
    { count: '1000+', label: 'Positive Reviews' }
  ];
  
</script>

<Header />
<Nav />

  <div class="container">
    <div class="mt-3 ml-5">
      <h1 class="font-extrabold">Find Clothes that matches your style!</h1>
      <p class="pt-5">Discover curated collections tailored to your personality, mood, and lifestyle. From everyday essentials to bold statement pieces, we've got everything you need to express yourself confidently.
      </p>
      <a href="#" class="bg-blue-950 text-center text-white px-10 py-2.5 mt-5 rounded-full inline-block">
        Shop Now
      </a>
    </div>
  </div>
  <section>
  <ul class="flex gap-8 pt-4 pl-5">
    {#each stats as stat}
      <StatItem count={stat.count} label={stat.label} />
    {/each}
  </ul>
</section>

<style>
  
</style>
