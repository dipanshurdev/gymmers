<script>
  import "../app.css";
  import CtAs from "../components/CTAs.svelte";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  import { openModal } from "../utils/index";

  let y;
  $: outerHeight = 0;

  function reroute(href) {
    $openModal = false;
    window.location.href = href;
  }
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 px-8 md:hidden"
  >
    <div class="flex items-center justify-between gap-4 border-b p-4 py-6">
      <a
        href="/"
        class="border border-slate-200 rounded-lg flex-center hover:border-blue-500 px-4 py-2"
      >
        <h1 class="font-semibold text-2xl">
          Gym<span class="text-blue-500">mers</span>
        </h1>
      </a>
      <button
        class="outline-none border-none"
        on:click={() => ($openModal = false)}
      >
        <i class="fa-solid fa-xmark text-2xl"></i>
      </button>
    </div>
    <div class="flex flex-col gap-4 flex-1">
      <button
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
        on:click={() => reroute("#product")}
      >
        <p
          class="duration-200 group-hover:pl-2
          flex
          items-center
          justify-start
          gap-4"
        >
          <span class="text-2xl font-semibold capitalize"> Product </span>
          <i class="fa-solid fa-chevron-right pl-4"></i>
        </p>
      </button>
      <button
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
        on:click={() => reroute("#review")}
      >
        <p
          class="duration-200 group-hover:pl-2 flex items-center justify-start gap-4"
        >
          <span class="text-2xl font-semibold capitalize"> Review </span>
          <i class="fa-solid fa-chevron-right pl-4"></i>
        </p>
      </button>
      <button
        class="border-none outline-none p-2 group duration-200 cursor-pointer text-left"
        on:click={() => reroute("#faqs")}
      >
        <p
          class="duration-200 group-hover:pl-2 flex items-center justify-start gap-4"
        >
          <span class="text-2xl font-semibold capitalize"> FAQs </span>
          <i class="fa-solid fa-chevron-right pl-4"></i>
        </p>
      </button>
    </div>
    <div class="py-4">
      <CtAs />
    </div>
  </div>
{/if}

{#if y > outerHeight}
  <div
    class="bg-slate-50 fixed top-0 left-0 w-full flex flex-col z-20 py-2 max-w-[1400px] fadeIn auto"
  >
    <Header />
  </div>
{/if}
<slot />
<Footer />
<svelte:window bind:scrollY={y} bind:outerHeight />
