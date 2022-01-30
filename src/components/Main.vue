<template>
  <div class="h-full w-full relative overflow-y-scroll">
    <Header />
    <div class="px-6 py-3 flex items-center justify-between">
      <h1
        class="text-white text-2xl font-semibold tracking-wider hover:underline pl-2"
      >
        Recently Played
      </h1>
      <h2
        class="text-sm hover:underline tracking-wider uppercase text-lightest"
      >
        See All
      </h2>
    </div>
    <div class="w-full flex flex-wrap pl-2">
      <div
        ref=""
        v-for="recent in recents"
        :key="recent.title"
        class="p-2 w-64 mx-2 my-2"
      >
        <div
          class="bg-light w-full h-auto p-5 rounded-lg shadow-md hover:bg-gray-700"
        >
          <img
            :src="`${recent.src}`"
            class="h-auto w-full rounded-lg shadow mb-2"
          />
          <h1 class="text-sm font-semibold text-white tracking-wide">
            {{ recent.title }}
          </h1>
          <h2 class="text-xs text-lightest tracking-wide">
            {{ recent.artist }}
          </h2>
        </div>
      </div>
    </div>
    <div class="px-6 py-3 flex items-center justify-between mt-5">
      <h1
        class="text-white text-2xl font-semibold tracking-wider hover:underline pl-2"
      >
        Shows to try
      </h1>
      <h2
        class="text-sm hover:underline tracking-wider uppercase text-lightest"
      >
        See All
      </h2>
    </div>
    <div class="w-full flex flex-wrap pl-2">
      <div
        ref=""
        v-for="recent in recents"
        :key="recent.title"
        class="p-2 w-64 mx-2 my-2"
      >
        <div
          class="bg-light w-full h-auto p-5 rounded-lg shadow-md hover:bg-gray-700"
        >
          <img
            :src="`${recent.src}`"
            class="h-auto w-full rounded-lg shadow mb-2"
          />
          <h1 class="text-sm font-semibold text-white tracking-wide">
            {{ recent.title }}
          </h1>
          <h2 class="text-xs text-lightest tracking-wide">
            {{ recent.artist }}
          </h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";

export default {
  name: "Main",
  components: {
    Header,
  },
  data: function () {
    return {
      recents: [
        {
          src: require("../assets/guddu.png"),
          title: "Virus 2062",
          artist: "Spotify Studios",
        },
        {
          src: require("../assets/horror.png"),
          title: "Horror Time",
          artist: "Sarthak Mishra",
        },
        {
          src: require("../assets/podcast.png"),
          title: "The Mythpat",
          artist: "Spotify Studios",
        },
        {
          src: require("../assets/ranveer.png"),
          title: "The Ranveer Show",
          artist: "BeerBiceps",
        },
        {
          src: require("../assets/tamil.png"),
          title: "Nallanna Murukku",
          artist: "Spotify Studios",
        },
      ],
    };
  },
};
</script>
