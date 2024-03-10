<script>
  const navLinks = [
    {
      text: "Home",
      href: "/",
    },
    {
      text: "Product",
      href: "/product",
    },
    {
      text: "Review",
      href: "/review",
    },
    {
      text: "FAQs",
      href: "/faqs",
    },
  ];
</script>

<header class="flex flex-col relative z-20">
  <div class="max-w-[1400px] mx-auto w-full flex justify-between p-4 py-6">
    <a href="/">
      <h1 class="font-semibold text-2xl">
        Gym
        <span class="text-blue-500">mers</span>
      </h1>
    </a>

    <button class="md:hidden grid place-items-center">
      <i class="fa-solid fa-bars text-xl"></i>
    </button>

    <nav class="hidden md:flex items-center justify-center lg:gap-6 gap-4">
      {#each navLinks as links}
        <li class="duration-200 hover:text-blue-500 cursor-pointer list-none">
          <a href={links.href} class="">
            {links.text}
          </a>
        </li>
      {/each}
    </nav>
  </div>
</header>
