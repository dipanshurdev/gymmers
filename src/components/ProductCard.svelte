<script>
  //   export let index;
  export let feat;
  export let index;
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-16">
  <div class="flex flex-col gap-8 md:gap-10">
    <h4
      class="text-2xl sm:text-3xl md:text-4xl max-w-[1000px] w-full font-medium relative pr-10 after:absolute after:top-full after:left-0 after:w-1/5 after:h-1/5 after:mt-1
 after:bg-slate-900"
    >
      <slot />
    </h4>
    <p>{feat.desc}</p>
    <div class="flex flex-col gap-3">
      {#each feat.featureList as list}
        <div class="flex gap-2 items-center">
          <div
            class="grid place-items-center px-1.5 text-xs sm:text-sm aspect-square rounded-full border-[1.5px] bg-white border-solid border-indigo-500"
          >
            <i class=" fa-solid fa-bolt text-indigo-900"></i>
          </div>
          <p>{list}</p>
        </div>
      {/each}
    </div>
  </div>
</div>
