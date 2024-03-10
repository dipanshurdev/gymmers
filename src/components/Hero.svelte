<script>
  import CtAs from "./CTAs.svelte";
  import Header from "./Header.svelte";
  import Wrapper from "./Wrapper.svelte";

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

<Wrapper id="home">
  <Header />
  <div
    class="flex flex-col flex-1 max-w-[1400px] mx-auto w-full items-center justify-center"
  >
    <h2
      class=" text-4xl sm:text-6xl md:text-6xl lg:text-8xl max-w-[1400px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-blue-500"> GYMMING </span>
      Is
      <span class="text-slate-700 line-through"> Hard </span> <br />
      Just Go
      <span class="text-blue-500"> Easier </span>
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl
     text-center max-w-[1200px] mx-auto w-full text-slate-700 my-4"
    >
      A dynamic image capturing the <span
        class="italic text-slate-900 font-bold capitalize"
      >
        energy and enthusiasm of individuals engaged in various fitness
        activities at Gymmers.
      </span>
      This could include people lifting weights, participating in group , and using
      cardio equipment, all with bright smiles on their faces.
    </p>
    <CtAs />
    <div class="flex items-center justify-center text-base w-2/4 flex-row py-4">
      <p>4,6</p>
      {#each ratings as star}
        <div class="grid place-items-center relative w-5 h-3">
          <div
            class="absolute top-0 left-0 grid place-items-center pr-2 justify-center w-8"
          >
            <i class={star.icon}></i>
          </div>
        </div>
      {/each}
      <p>4k+</p>
    </div>
  </div>
</Wrapper>
