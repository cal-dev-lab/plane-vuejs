<template>
  <header class="sticky top-0 z-30">
    <nav className="bg-white shadow-sm border-b-2 border-gray-200">
      <div className="max-w-6xl px-8 mx-auto">
        <div className="flex justify-between">
          <div className="flex space-x-4">
            <div className="">
              <a href="/#" className="flex items-center py-5 px-2 text-gray-700">
                <span
                  className="font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500 text-xl hover:text-indigo-600 transition duration-300"
                >
                  air11-UK
                </span>
              </a>
            </div>

            <div className="hidden md:flex items-center space-x-1 pl-10">
              <a
                className="uppercase tracking-wide text-xs tracking-widest py-5 px-3 hover:underline hover:text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500 transition duration-500"
              >
                <router-link to="/">Home</router-link>
              </a>
              <a
                className="uppercase tracking-wide text-xs tracking-widest py-5 px-3 hover:underline hover:text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500 transition duration-500"
              >
                <router-link to="planes">Planes</router-link>
              </a>
              <a
                className="uppercase tracking-wide text-xs tracking-widest py-5 px-3 hover:underline hover:text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500 transition duration-500"
              >
                <router-link to="about">About</router-link>
              </a>

              <a
                className="uppercase tracking-wide text-xs tracking-widest py-5 px-3 hover:underline hover:text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500 transition duration-500"
              >
                <router-link to="blog">Blog</router-link>
              </a>
            </div>
          </div>

          <div className="md:hidden flex items-center">
            <button onClick="{mobileClick}" className="mobile-menu-button">
              <svg
                class="w-6 h-6 text-black hover:text-blue-700 transition duration-300"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16m-7 6h7"
                ></path>
              </svg>
            </button>
          </div>
        </div>
      </div>

      <div className="mobile-menu hidden md:hidden">
        <a
          className="block uppercase tracking-wide py-6 px-24 text-sm tracking-widest bg-gradient-to-r from-red-500 to-pink-500 text-white hover:from-white hover:to-white hover:text-black transition duration-500"
        >
          <router-link to="/">Home</router-link>
        </a>
        <a
          className="block uppercase tracking-wide py-6 px-24 text-sm tracking-widest bg-gradient-to-r from-red-500 to-pink-500 text-white hover:from-white hover:to-white  hover:text-black transition duration-500"
        >
          <router-link to="/blog">Blog</router-link>
        </a>
        <a
          className="block uppercase tracking-wide py-6 px-24 text-sm tracking-widest bg-gradient-to-r from-red-500 to-pink-500 text-white hover:from-white hover:to-white rounded-b-xl shadow-xl hover:text-black transition duration-500"
        >
          <router-link to="/about">About</router-link>
        </a>
        <a
          className="block uppercase tracking-wide py-6 px-24 text-sm tracking-widest bg-gradient-to-r from-red-500 to-pink-500 text-white hover:from-white hover:to-white rounded-b-xl shadow-xl hover:text-black transition duration-500"
        >
          <router-link to="/planes">Planes</router-link>
        </a>
      </div>
    </nav>
  </header>
</template>

<script type="text/js">
export default {
  name: "NavBar",
  methods: {}
};
</script>
