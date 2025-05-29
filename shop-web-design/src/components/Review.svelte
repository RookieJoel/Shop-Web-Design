<script lang="ts">
    import { Card } from "flowbite-svelte";
    export let src: string;
    export let username: string;
    export let text_header: string;
    export let review: string;
</script>

<Card size="xl" class="py-5 px-2 bg-white dark:bg-gray-800 rounded-lg shadow">
  <figure class="flex flex-col items-center text-center">
    <blockquote class="mb-4 text-gray-500 dark:text-gray-400">
      <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{text_header}</h3>
      <p class="mt-2 font-light">{review}</p>
    </blockquote>
    <figcaption class="flex items-center justify-center space-x-3 mt-4">
      <img class="h-10 w-10 rounded-full" src={src} alt={username} />
      <div class="text-left font-medium dark:text-white">
        <div>{username}</div>
      </div>
    </figcaption>
  </figure>
</Card>
