<script lang="ts">
  import { Card, Button, Rating, Badge } from "flowbite-svelte";
  export let ImgSrc: string;
  export let text: string;
  export let rating: number;
  export let size: number;
  export let price:number;
</script>

<Card class="p-0 m-2">
  <a href="/">
    <img class="rounded-t-lg p-4" src={ImgSrc}/>
  </a>
  <div class="px-5 pb-2">
    <a href="/">
      <h5 class="text-2xl font-extrabold tracking-tight text-gray-900 dark:text-white">{text}</h5>
    </a>
    <Rating {rating} {size} class="mt-2 mb-3">
      {#snippet text()}
        <Badge class="ms-3">{rating}</Badge>
      {/snippet}
    </Rating>
    <div class="flex items-center justify-between">
      <span class="text-3xl font-bold text-gray-900 dark:text-white">{price}$</span>
      <Button href="/">Buy now</Button>
    </div>
  </div>
</Card>
