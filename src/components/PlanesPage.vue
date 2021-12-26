<template>
  <div class="text-center mx-auto mt-20 mb-20">
    <h1
      class="text-2xl uppercase tracking-widest font-bold mb-2 text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500"
    >
      New planes
    </h1>
    <p class="text-sm text-gray-600">The latest and greatest planes from 1970 - present.</p>
  </div>
  <div class="flex items-center mx-auto">
    <div class="flex-1 max-w-6xl mx-auto p-10 items-center">
      <ul class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3 px-2">
        <div v-if="planeitems.length">
          <div :key="planeitem.index" v-for="planeitems in planeitems">
            <li class="mx-auto items-center p-2 rounded-lg md:h-full h-full">
              <img :src="imageLink + planeitem.image" width="450" height="250" top alt="{{ planeitem.title }}" />
              <h5 class="text-lg font-bold mt-2 text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500">{{ planeitem.title }}</h5>
              <p class="text-sm mx-auto mt-2">
              {{ planeitem.description }}
              </p>
            </li>
          </div>
        </div>
      </ul>
    </div>
  </div>
</template>






<!-- OLD DATA -->
        <!-- START: Loop over JSON in <script> and spit out data -->
        <!-- <div v-for="plane in planes" :key="plane.id" class="plane">
          <li class="mx-auto items-center p-2 rounded-lg md:h-full h-full">
            <img :src="plane.image" width="450" height="250" />
            <h5 class="text-lg font-bold mt-2 text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-500">{{ plane.title }}</h5>
            <p class="text-sm mx-auto mt-2">
              @TODO: Add description in JSON <script> 
              A paragraph containing information about the model variant.
            </p>
          </li>
        </div> -->
        <!-- END: Loop over JSON in <script> and spit out data -->
<!-- OLD DATA -->






<script>
export default {
  data() {
    return {
      planeitems: [],
      imageLink: "http://localhost:1337/api/planeitems/"
    }
  },
  mounted() {
    fetch("http://localhost:1337/api/planeitems")
    .then((res) => res.json())
    .then((data) => {
      this.planeitems = data;
    });
  }



  // OLD DATA
  // data() {
  //   return {
  //     // START: Data for planes
  //     planes: [
  //       { title: 'ATR-42', id: 1, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'ATR-72', id: 2, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A220', id: 3, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A300', id: 4, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A310', id: 5, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A318', id: 6, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A319', id: 7, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A320', id: 8, image: 'https://via.placeholder.com/450x250' },
  //       { title: 'Airbus A321', id: 9, image: 'https://via.placeholder.com/450x250' }
  //     ],
  //     // END: Data for planes
  //   };
  // },
};
</script>
