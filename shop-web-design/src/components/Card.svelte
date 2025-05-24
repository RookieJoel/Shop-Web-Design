<script lang="ts">
  export let ImgSrc: string;
  export let text: string;
</script>

<div class="grid grid-cols-4 gap-4 p-4 text-white">
  <div class="bg-">
    <img src={ImgSrc} alt="Image" class="w-full h-auto rounded" />
  </div>

  <div class="flex items-center">
    <img src={ImgSrc} alt="Image" class="w-full h-auto rounded" />
  </div>

  <div class="flex items-center justify-center">
    <img src={ImgSrc} alt="Image" class="w-full h-auto rounded" />
  </div>

  <div class="flex items-center justify-center">
    <img src={ImgSrc} alt="Image" class="w-full h-auto rounded" />
  </div>
</div>
