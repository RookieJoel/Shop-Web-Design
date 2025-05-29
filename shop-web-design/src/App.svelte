<script lang="ts">
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import StatItem from "./components/StatItem.svelte";
  import Card from "./components/Card.svelte";
  import Review from "./components/Review.svelte";
  import Footer from "./components/Footer.svelte";
  const stats = [
    { count: "1100+", label: "Happy Customers" },
    { count: "800+", label: "Projects Completed" },
    { count: "1000+", label: "Positive Reviews" },
  ];

  const reviews = [
    {
      src: "https://placehold.co/100x100",
      username: "John Doe",
      text_header: "Amazing Service!",
      review:
        "I had a fantastic experience shopping here. The quality of the clothes is top-notch and the customer service is exceptional.",
    },
    {
      src: "https://placehold.co/100x100",
      username: "Jane Smith",
      text_header: "Stylish and Affordable",
      review:
        "I love the variety of styles available. I found exactly what I was looking for at a great price!",
    },
    {
      src: "https://placehold.co/100x100",
      username: "Alice Johnson",
      text_header: "Highly Recommend",
      review:
        "The shopping experience was seamless. Fast shipping and the clothes fit perfectly!",
    },
    {
      src: "https://placehold.co/100x100",
      username: "Bob Brown",
      text_header: "Quality Products",
      review:
        "I was impressed with the quality of the fabrics. Will definitely shop here again!",
    },
  ];
</script>

<Header />
<Nav />

<div class="w-full bg-neutral-300">
  <div
    class="container mx-auto flex flex-wrap items-center justify-between px-4 py-8"
  >
    <section class="mt-3 max-w-xl ml-15">
      <h1 class="font-extrabold text-6xl">
        Find clothes that matches your style!
      </h1>
      <p class="pt-5">
        Discover curated collections tailored to your personality, mood, and
        lifestyle. From everyday essentials to bold statement pieces, we've got
        everything you need to express yourself confidently.
      </p>
      <a
        href="#"
        class="w-full md:w-auto bg-blue-950 text-center text-white px-10 py-2.5 mt-5 rounded-full inline-block"
      >
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

    <section class="mt-3 mr-3 justify-center">
      <img
        src="/fashion_preview-removebg-preview.png"
        alt="Fashion preview"
        class="rounded-xl"
      />
    </section>
  </div>
</div>

<div class="bg-gray-800 text-center text-white py-4">
  <h2 class="font-bold text-3xl">New Arrivals</h2>
</div>

<section
  class="container mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-4 justify-items-center"
>
  <Card
    ImgSrc="/Jacket.png"
    text="Stylish Jacket"
    rating={4.5}
    size={24}
    price={49.99}
  />
  <Card
    ImgSrc="/Sneaker.png"
    text="Casual Sneakers"
    rating={4.0}
    size={24}
    price={59.99}
  />
  <Card
    ImgSrc="/Dress.png"
    text="Elegant Dress"
    rating={5.0}
    size={24}
    price={79.99}
  />
  <Card
    ImgSrc="/Jean.png"
    text="Perfect Jean"
    rating={4.2}
    size={24}
    price={39.99}
  />
  <div class="col-span-full flex justify-center">
    <button
      class="bg-blue-950 text-white px-4 py-3 rounded-lg hover:bg-blue-800 transition duration-300"
    >
      View All Products
    </button>
  </div>
</section>

<section>
  <div class="container">
    <div class="bg-gray-200 text-center py-8 p rounded-3xl">
      <h2 class="text-3xl font-bold mb-4">Find Your Fit</h2>
      <h3 class="text-xl mb-6 font-bold">Flaunt Your Style</h3>
      <div class="grid grid-cols-1 md:grid-cols-4 md:grid-rows-2 gap-4 p-3">

        <div class="style-item md:col-span-2 bg-[url('/Casual.png')]">
          <h4 class="text-xl font-semibold">Casual Wear</h4>
        </div>

        <div class="style-item  md:row-span-2 bg-[url('/Formal.png')] tall ">
          <h4 class="text-xl font-semibold">Formal Wear</h4>
        </div>

        <div class="style-item  md:row-span-2 bg-[url('/sport.png')] tall ">
          <h4 class="text-xl font-semibold">Sportswear</h4>
        </div>

        <div class="style-item bg-[url('/ring.png')]">
          <h4 class="text-xl font-semibold">Accessories</h4>
        </div>

        <div class="style-item bg-[url('/Shoes.png')]">
          <h4 class="text-xl font-semibold">Footwear</h4>
        </div>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container mx-auto py-8">
    <h2 class="md:text-4xl font-extrabold mx-15">Customers Reviews</h2>
    <p class="md:text-lg mb-6 mx-15">
      See what our customers are saying about us!
    </p>
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mx-15">
      {#each reviews as review}
        <Review {...review} />
      {/each}
    </div>
  </div>
</section>

<Footer />
