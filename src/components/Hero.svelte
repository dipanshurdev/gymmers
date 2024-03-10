<script>
  import CtAs from "./CTAs.svelte";
  import Header from "./Header.svelte";
  import Wrapper from "./Wrapper.svelte";
</script>

<Wrapper id="home">
  <Header />
  <div
    class="flex flex-col flex-1 max-w-[1400px] mx-auto w-full items-center justify-center"
  >
    <h2
      class=" text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-blue-500"> GYMMING </span>
      Is
      <span class="text-slate-700 line-through"> Hard </span> <br />
      Just Go
      <span class="text-blue-500"> Easier </span>
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl
     text-center max-w-[1000px] mx-auto w-full text-slate-700"
    >
      A dynamic image capturing the <span
        class="italic text-slate-900 font-bold capitalize"
      >
        energy and enthusiasm of individuals engaged in various fitness
        activities at Gymmers.
      </span>
      This could include people lifting weights, doing yoga, participating in group
      classes, and using cardio equipment, all with bright smiles and determination
      on their faces.
    </p>
    <CtAs />
    <div class="flex items-center justify-center gap-2 text-base">
      <p>4,6</p>
      {#each Array.from({ length: 5 }) as index}
        <div class="grid place-items-center relative">
          <i class="fa-solid fa-star opacity-0"></i>
          <div
            class={`absolute top-0 left-0 grid place-items-center ${index === 4 ? "w-[50%] overflow-hidden " : ""}`}
          >
            <i class="fa-solid fa-star text-amber-400"></i>
          </div>
        </div>
      {/each}
    </div>
  </div>
</Wrapper>
