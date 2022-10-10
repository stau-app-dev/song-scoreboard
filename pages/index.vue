<template>
  <div class="flex min-h-screen flex-col">
    <Fullscreen v-if="!isFullscreen" />
    <Header />
    <div class="flex flex-1 flex-col space-y-4 py-6 px-16">
      <h3 class="text-center text-4xl font-extralight">
        Upvote songs on the school app!
      </h3>
      <h4 class="text-center text-3xl">
        The
        <span class="underline decoration-dotted">top three songs</span> (min.
        300 votes) will be selected for an upcoming LIVE performance.
      </h4>
      <div class="flex-1 py-3 text-center">
        <Scoreboard :songs="songs" />
        <h5 class="text-2xl font-extralight mt-6 italic">
          (Live Scoreboard - updated every 30 seconds)
        </h5>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      windowHeight: window.innerHeight,
      songs: [],
    };
  },
  async fetch() {
    const response = await this.$axios.get('/getSongs');
    const songs = response.data.data;
    this.songs = songs.slice(0, 5);
  },
  computed: {
    isFullscreen() {
      if ((screen.availHeight || screen.height - 50) <= this.windowHeight) {
        return true;
      }
      return false;
    },
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
      setInterval(() => {
        this.$fetch();
      }, 30000);
    });
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.onResize);
  },
  methods: {
    onResize() {
      this.windowHeight = window.innerHeight;
    },
  },
};
</script>
