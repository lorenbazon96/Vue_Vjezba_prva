<template>
  <div class="flex items-center justify-center mx-0 my-0 blok">
    <div class="text-center">
      <button @click="toggleDarkMode" class="btn btn-danger">
        {{ isDarkMode ? "light" : "dark" }} mod
      </button>
      <h1 class="text-[3.75rem] mb-4 italic">
        Pozdrav, ja sam
        <span class="text-red-700 font-bold">Loren Bažon</span>
      </h1>
      <hr class="mb-2 border-red-700 border-4" />
      <h2 class="text-[1.5rem] mb-3 italic text-start blok">
        Moji omiljeni filmovi:
      </h2>

      <div class="container py-1">
        <div class="row">
          <div class="col-12 col-md-4">
            <img
              src="https://upload.wikimedia.org/wikipedia/bs/9/9c/Prebrzi_i_prezestoki.jpg"
              class="img-fluid rounded-md mx-auto"
              style="height: 480px; object-fit: cover"
              alt="film1"
            />

            <p class="text-[1.25rem] italic pt-2 pb-8 blok">2 Fast 2 Furious</p>
          </div>

          <div class="col-12 col-md-4">
            <img
              src="https://upload.wikimedia.org/wikipedia/en/d/d8/The_Wolf_of_Wall_Street_%282013%29.png"
              class="img-fluid rounded-md mx-auto"
              style="height: 480px; object-fit: cover"
              alt="film2"
            />
            <p class="text-[1.25rem] italic pt-2 pb-8 blok">
              The Wolf of Wall Street
            </p>
          </div>

          <div class="col-12 col-md-4">
            <img
              src="https://upload.wikimedia.org/wikipedia/en/4/49/Pain_%26_Gain_film_poster.jpg"
              class="img-fluid rounded-md mx-auto"
              style="height: 480px; object-fit: cover"
              alt="film3"
            />

            <p class="text-[1.25rem] italic pt-2 pb-8 blok">Pain & Gain</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      isDarkMode: false,
    };
  },
  methods: {
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
      if (this.isDarkMode) {
        document.documentElement.classList.add("dark");
      } else {
        document.documentElement.classList.remove("dark");
      }
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.blok {
  background-color: rgb(219, 219, 219);
  color: rgb(26, 26, 26);
  padding: 20px;
  margin-top: 20px;
  border-radius: 8px;
}

.dark .blok {
  background-color: #111;
  color: white;
}
</style>
