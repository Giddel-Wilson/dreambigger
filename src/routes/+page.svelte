<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<main
  class="main min-h-screen bg-[#EEE9E5] flex items-center justify-center overflow-hidden p-5"
>
  <div
    class="container w-[80vw] mx-auto px-5 py-5 shadow-lg border rounded-3xl bg-[whitesmoke]"
  >
    <!-- Navbar -->
    <nav
      class="h-[10vh] z-50 flex justify-between items-center py-4 opacity-0 animate-fadeIn delay-200"
    >
      <!-- Mobile Hamburger Icon -->
      <div class="hbg lg:hidden">
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
        >Get started</a
      >

      <!-- Mobile Menu Overlay -->
      <div
        class={`mobileMenu absolute top-0 left-0 w-3/4 h-full bg-white p-4 transition-transform transform ${isMenuOpen ? "translate-x-0" : "-translate-x-full"} lg:hidden border rounded-lg shadow-2xl z-[1000]`}
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
              >Get started</a
            >
          </li>
        </ul>
      </div>
    </nav>

    <section class="sec relative h-[75vh] py-3 flex flex-col align-middle justify-between">
      <!-- Background Image Section -->
      <div class="w-full h-full absolute inset-0 z-0">
        <enhanced:img
          src="../lib/assets/mac.jpg"
          alt="Background"
          class="mac w-full h-full object-cover border rounded-lg"
        />
      </div>

      <!-- Main content -->
      <div class="mc text-center mt-16 opacity-0 animate-slideInUp delay-300">
        <h1
          class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold text-gray-800 transition-transform transform hover:scale-105 duration-300"
        >
          Dream bigger
        </h1>
        <p
          class="mt-4 text-gray-500 opacity-0 animate-fadeIn delay-500 text-sm sm:text-base"
        >
          Start your free trial today. No credit card needed.
        </p>
        <button
          class="mt-6 px-4 py-2 sm:px-6 sm:py-3 bg-green-600 text-white rounded-full hover:bg-green-700 transition-transform transform hover:scale-105 duration-300"
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
            class="w-6 h-6 sm:w-7 sm:h-7 object-contain transition-transform transform hover:scale-110 hover:cursor-pointer"
            alt="stars"
          />
          <input
            class="px-4 sm:px-6 py-3 sm:py-4 rounded-lg text-gray-800 bg-transparent transition-transform transform hover:scale-105 duration-300"
            placeholder="Sveltekit prompt input."
          />
          <button
            class="ml-3 sm:ml-4 px-4 sm:px-6 py-3 sm:py-4 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-transform transform hover:scale-105 duration-300"
            >Generate</button
          >
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

  /* Media Queries for Mobile */
  @media (max-width: 890px) {
    .main {
      padding: 0;
      height: 100vh;
      width: 100vw;
    }

    .container {
      padding: 0;
      background-color: transparent;
      border: none;
      box-shadow: none;
      height: max-content;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 15px;
    }

    .nav {
      height: 10vh;
    }

    .sec {
      height: 90vh;
      width: 100vw;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      padding: 2em 0.3em;
      border-radius: 50px;
      position: inherit;
    }

    .mc {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 0.5em;
      padding: 0 1em;
    }

    .mobileMenu {
      border-top-left-radius: 0px;
      border-bottom-left-radius: 0px;
      z-index: 1000;
    }

    .mac {
      height: 100vh;
      width: 100vw;
    }

    h1 {
      font-size: 2rem;
    }

    p {
      font-size: 1rem;
    }

    button {
      font-size: 0.9rem;
    }

    .container {
      padding: 10px;
    }
  }

  @media (max-width: 640px) {
    .text-center {
      margin-top: 12px;
    }

    input {
      font-size: 0.8rem;
    }

    button {
      padding: 8px 12px;
    }
  }

  @media (max-width: 200px) {
    .main {
      padding: 0;
      overflow: hidden;
    }
    .main div {
      padding: 0;
    }
    h1 {
      font-size: 1.5rem;
    }
    .hbg button svg {
      height: 25px;
      width: auto;
    }
/* 
    p {
      font-size: 1rem;
    }

    button {
      font-size: 0.9rem;
    }

    .container {
      padding: 10px;
    } */
  }
</style>
