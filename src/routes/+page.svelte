<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<main
  class="min-h-screen bg-[#EEE9E5] flex items-center justify-center overflow-hidden p-5"
>
  <div
    class="container mx-auto px-10 py-5 shadow-lg border rounded-3xl bg-[whitesmoke]"
  >
    <!-- Navbar -->
    <nav
      class="flex justify-between items-center py-4 opacity-0 animate-fadeIn delay-200"
    >
      <!-- Mobile Hamburger Icon -->
      <div class="lg:hidden">
        <button
          on:click={toggleMenu}
          class="text-gray-800 focus:outline-none absolute top-7 left-4"
        >
          <svg
            class="h-8 w-8"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16m-7 6h7"
            />
          </svg>
        </button>
      </div>

      <!-- Desktop Links -->
      <ul class="hidden lg:flex space-x-8 text-sm text-gray-600">
        <li>
          <a href="./" class="hover:underline font-medium hover:font-bold"
            >Features</a
          >
        </li>
        <li>
          <a href="./" class="hover:underline font-medium hover:font-bold"
            >How to use</a
          >
        </li>
        <li>
          <a href="./" class="hover:underline font-medium hover:font-bold"
            >Licenses</a
          >
        </li>
        <li>
          <a href="./" class="hover:underline font-medium hover:font-bold"
            >Pricing</a
          >
        </li>
      </ul>

      <!-- Get Started Button -->
      <a
        href="./"
        class="bg-gray-200 px-4 py-2 rounded-full text-gray-800 text-sm hover:bg-gray-300 transition ease-in-out duration-300 hidden lg:block"
      >
        Get started
      </a>

      <!-- Mobile Menu Overlay -->
      <div
        class={`absolute top-0 left-0 w-3/4 h-full bg-white p-4 transition-transform transform ${
          isMenuOpen ? "translate-x-0" : "-translate-x-full"
        } lg:hidden border rounded-2xl shadow-2xl z-[1000]`}
      >
        <button
          on:click={toggleMenu}
          class="text-gray-800 mb-4 focus:outline-none"
        >
          <svg
            class="h-8 w-8"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
        <ul class="space-y-10 text-gray-600 text-center py-3">
          <li>
            <a href="./" class="hover:underline font-medium hover:font-bold"
              >Features</a
            >
          </li>
          <li>
            <a href="./" class="hover:underline font-medium hover:font-bold"
              >How to use</a
            >
          </li>
          <li>
            <a href="./" class="hover:underline font-medium hover:font-bold"
              >Licenses</a
            >
          </li>
          <li>
            <a href="./" class="hover:underline font-medium hover:font-bold"
              >Pricing</a
            >
          </li>
          <li>
            <a
              href="./"
              class="bg-gray-200 px-4 py-2 rounded-lg text-gray-800 hover:bg-gray-300 transition ease-in-out duration-300"
            >
              Get started
            </a>
          </li>
        </ul>
      </div>
    </nav>

    <section
      class="h-[75vh] relative py-3 flex flex-col align-middle justify-between"
    >
      <!-- Background Image Section -->
      <div class="w-full h-full absolute inset-0 z-0">
        <enhanced:img
          src="../lib/assets/mac.jpg"
          alt="Background"
          class="w-full h-full object-cover border rounded-lg"
        />
      </div>

      <!-- Main content -->
      <div class="text-center mt-16 opacity-0 animate-slideInUp delay-300">
        <h1
          class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-gray-800 transition-transform transform hover:scale-105 duration-300"
        >
          Dream bigger
        </h1>
        <p class="mt-4 text-gray-500 opacity-0 animate-fadeIn delay-500">
          Start your free trial today. No credit card needed.
        </p>
        <button
          class="mt-6 px-6 py-3 bg-green-600 text-white rounded-full hover:bg-green-700 transition-transform transform hover:scale-105 duration-300"
        >
          Join the waiting list
        </button>
      </div>

      <!-- Call-to-Action Buttons -->
      <div
        class="text-center mb-3 space-y-3 opacity-0 animate-slideInUp delay-800 flex justify-center"
      >
        <div
          class="flex items-center justify-center max-w-max bg-[rgba(255,255,255,0.5)] p-2 rounded-lg space-x-1"
        >
          <enhanced:img
            src="../lib/assets/stars.png"
            class=" w-7 h-7 object-contain transition-transform transform hover:scale-110 hover:cursor-pointer"
            alt="stars"
          />
          <input
            class="px-6 py-4 rounded-lg text-gray-800 bg-transparent transition-transform transform hover:scale-105 duration-300"
            placeholder="A minimalist mockup template!"
          />
          <button
            class="ml-4 px-6 py-4 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-transform transform hover:scale-105 duration-300"
          >
            Generate
          </button>
        </div>
      </div>
    </section>
  </div>
</main>

<style>
  a {
    text-underline-offset: 0.3em;
  }

  input {
    outline: none;
    border: none;
  }

  /* Animations */
  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @keyframes slideInUp {
    from {
      transform: translateY(30px);
      opacity: 0;
    }
    to {
      transform: translateY(0);
      opacity: 1;
    }
  }

  .animate-fadeIn {
    animation: fadeIn 1s forwards;
  }

  .animate-slideInUp {
    animation: slideInUp 1s forwards;
  }

  .delay-200 {
    animation-delay: 0.2s;
  }
  .delay-300 {
    animation-delay: 0.3s;
  }
  .delay-500 {
    animation-delay: 0.5s;
  }
  .delay-700 {
    animation-delay: 0.7s;
  }
  .delay-800 {
    animation-delay: 0.8s;
  }
</style>
