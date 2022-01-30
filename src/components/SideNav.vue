<template>
  <div class="w-56 bg-black h-full flex-none">
    <div class="p-6">
      <img
        class="h-10"
        src="../assets/spotify-logo-white.png"
        style="filter: brightness(0) invert(1)"
      />
    </div>
    <div class="mx-2">
      <button
        v-for="page in pages"
        :key="page.id"
        @click="setID = page.id"
        :class="`w-full rounded px-3 py-2 flex items-center mb-2 justify-start h-10 text-s font-semibold ${
          setID === page.id ? 'bg-light text-white' : 'text-lightest'
        }`"
      >
        <div class="icons px-3">
          <fa v-if="page.name == 'Home'" icon="home"> </fa>
          <fa v-if="page.name == 'Search'" icon="search"> </fa>
          <fa v-if="page.name == 'Library'" icon="list-ul"> </fa>
        </div>
        <p class="px-2">{{ page.name }}</p>
      </button>
    </div>
    <div class="mx-5">
      <h1
        class="text-xs text-lightest px-3 mt-8 mb-3 tracking-widest uppercase"
      >
        Playlist
      </h1>
      <button
        class="mb-2 opacity-75 hover:opacity-100 flex items-center text-white justify-start h-10 w-full rounded px-3 text-s font-semibold"
      >
        <fa icon="plus" color="#B3B3B3"> </fa>
        <p class="ml-5">Create Playlist</p>
      </button>
      <button
        class="opacity-75 hover:opacity-100 flex items-center justify-start text-white h-10 w-full rounded px-3 text-s font-semibold"
      >
        <fa icon="heart" color="#B3B3B3"> </fa>
        <p class="ml-5">Liked Songs</p>
      </button>
      <div class="h-px w-full bg-light my-3"></div>
    </div>
    <div class="mx-5">
      <div class="w-full h-10 overflow-y-scroll ml-3">
        <p
          v-for="album in albums"
          :key="album.name"
          class="text-lightest hover:text-white text-s py-1 font-semibold"
        >
          {{ album.name }}
        </p>
      </div>
      <button
        class="opacity-75 hover:opacity-100 flex items-center justify-start ml-3 text-s text-white font-semibold mt-2"
      >
        <fa icon="arrow-alt-circle-down" color="#B3B3B3"> </fa>
        <p class="pl-5">Install App</p>
      </button>
    </div>
    <div class="relative pt-20 mt-3">
      <div class="absolute w-full h-full flex">
        <div class="pl-48 pt-1 opacity-0 hover:opacity-100">
          <fa icon="chevron-down" color="#B3B3B3" size="2x" />
        </div>
      </div>
      <img src="../assets/playing.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SideNav",
  data: function () {
    return {
      pages: [
        {
          id: "home",
          name: "Home",
          icon: "home",
        },
        {
          id: "search",
          name: "Search",
          icon: "search",
        },
        {
          id: "library",
          name: "Library",
          icon: "list-ul",
        },
      ],
      setID: "home",
      albums: [
        { name: "Rock" },
        { name: "Indie" },
        { name: "Romantic" },
        { name: "Pop" },
        { name: "Gazal" },
      ],
    };
  },
};
</script>
