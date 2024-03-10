<script>
  import { fade } from "svelte/transition";
  import ProductCard from "./ProductCard.svelte";
  import Wrapper from "./Wrapper.svelte";

  let features = [
    {
      featureList: [
        "Daily streak counter",
        "Weights and reps tracker",
        "Community challenges",
        "Begginer friendly exercieses",
      ],
      desc: "We ensures all users have the information they need to train safely and train effectively.",
      imgUrl: "",
    },
    {
      featureList: [
        "Select your preferences",
        "Personalize your workouts",
        "Customize your training",
        "Guarantees progress on all core exercises",
      ],
      desc: "Build your streaks and see your progress with our amazing tracking and analytics features.",
      imgUrl: "",
    },
    {
      featureList: [
        "Eliminating gusswork",
        "Save your time",
        "Archive the perfect seek",
        "Builds function strength",
      ],
      desc: "Enter as much information about yourself as you desire to ensure all workouts are personalized to your every need.",
      imgUrl: "",
    },
  ];
</script>

<Wrapper id="project">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your <span class="text-blue-500"> fitness journey </span>
        with us today!
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Features for Everyone
      </h3>
    </div>
  </div>
  <div
    class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-16 lg:gap-20 relative text-base"
  >
    {#each features as feat, index}
      <ProductCard {feat} {index}>
        <!-- {#if index === 0}
          Experience a beginner exercise <span
            class="text-indigo-400 font-medium">master</span
          > class
        {:else if index === 1}
          Lay the foundations for <span class="text-indigo-400 font-medium"
            >routine</span
          > and consistency
        {:else}
          Workouts specific to your <span class="text-indigo-400 font-medium"
            >environment</span
          >
          and
          <span class="text-indigo-400 font-medium">expertise</span>
        {/if} -->
      </ProductCard>
    {/each}
  </div>
</Wrapper>
