<script>
  import CtAs from "./CTAs.svelte";
  import Header from "./Header.svelte";

  import Stars from "./Stars.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
</script>

<SectionWrapper id="home">
  <Header />
  <div
    class="flex flex-col flex-1 max-w-[1400px] mx-auto w-full items-center justify-center"
  >
    <h2
      class=" text-4xl sm:text-6xl md:text-6xl lg:text-8xl max-w-[1400px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-blue-500"> GYMMING </span>
      Is
      <span class="text-slate-700 line-through"> Hard </span> <span></span>

      <br />
      Just Got
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
      <Stars />
    </div>
  </div>
</SectionWrapper>
