<script>
  const ratings = [
    {
      icon: "fa-solid fa-star text-amber-400",
    },
    {
      icon: "fa-solid fa-star text-amber-400",
    },
    {
      icon: "fa-solid fa-star text-amber-400",
    },
    {
      icon: "fa-solid fa-star text-amber-400",
    },
    {
      icon: "fa-solid fa-star-half text-amber-400",
    },
  ];
</script>

<div class="flex items-center justify-center gap-2 text-base">
  <p>4.5</p>
  {#each ratings as star}
    <div class="grid place-items-center relative">
      <i class="fa-solid fa-star opacity-0"></i>
      <div
        class={"absolute top-0 left-0 grid place-items-center " +
          (star === 4 ? "w-[60%] overflow-hidden" : " ")}
      >
        <i class={star.icon}></i>
      </div>
    </div>
  {/each}
  <p>50k+</p>
</div>
