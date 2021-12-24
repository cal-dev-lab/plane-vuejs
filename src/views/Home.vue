<template>
  <div class="home">
    <div id="particle" class="px-2 max-w-6xl min-h-screen mx-auto items-center justify-center">
        <div class="relative -mt-20 top-40 sm:top-60 md:top-80">
          <ul class="grid grid-cols-1 p-4">
            <!-- START: Loop over JSON in <script> and spit out data -->
            <div class="flex gap-8 items-center text-center justify-center">
              <li class="text-center items-center justify-center">
                <h5 class="text-4xl sm:text-6xl uppercase tracking-tighter font-bold">" Welcome "</h5>
              </li>
            </div>
            <div>
              <li class="text-center items-center justify-center">
                <p class="text-sm mx-auto mt-2">
                air11-uk invites you to 
                <a class="underline text-red-500">
                  <router-link to="planes">explore all of the planes in existence</router-link>
                </a>
                </p>
              </li>
            </div>
          </ul>
        </div>
      <VueParticle domId='particle' :config=particleConfig />
    </div>
  </div>
</template>

<script>
import VueParticle from 'vue-particlejs'

export default {
  name: "home",
  components: {
    VueParticle,
  },
  data: function() {
    return {
        particleConfig: {
        particles: {
          number: { value: 300, density: { enable: true, value_area: 800 } },
          color: { value: "#000" },
          shape: {
            type: "circle",
            stroke: { width: 0, color: "#000000" },
            polygon: { nb_sides: 5 },
            image: { src: "img/github.svg", width: 100, height: 100 }
          },
          opacity: {
            value: 0.5,
            random: false,
            anim: { enable: false, speed: 1, opacity_min: 0.1, sync: false }
          },
          size: {
            value: 3,
            random: true,
            anim: { enable: false, speed: 40, size_min: 0.1, sync: false }
          },
          line_linked: {
            enable: true,
            distance: 150,
            color: "#000",
            opacity: 0.4,
            width: 1
          },
          move: {
            enable: true,
            speed: 6,
            direction: "none",
            random: false,
            straight: false,
            out_mode: "out",
            bounce: false,
            attract: { enable: false, rotateX: 600, rotateY: 1200 }
          }
        },
        interactivity: {
          detect_on: "canvas",
          events: {
            onhover: { enable: true, mode: "repulse" },
            onclick: { enable: true, mode: "push" },
            resize: true
          },
          modes: {
            grab: { distance: 400, line_linked: { opacity: 1 } },
            bubble: {
              distance: 400,
              size: 40,
              duration: 2,
              opacity: 8,
              speed: 3
            },
            repulse: { distance: 200, duration: 0.4 },
            push: { particles_nb: 4 },
            remove: { particles_nb: 2 }
          }
        },
        retina_detect: true
      }
    };
  }
};
</script>
