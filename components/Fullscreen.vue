<template>
  <div
    class="fixed bg-primary min-h-full w-full z-50 flex justify-center items-center"
  >
    <h1 class="text-6xl text-white font-bold">Click to go to fullscreen.</h1>
  </div>
</template>

<script>
export default {
  name: 'FullscreenComponent',
  mounted() {
    document.addEventListener('click', () => {
      const el = document.documentElement;
      const rfs =
        el.requestFullScreen ||
        el.webkitRequestFullScreen ||
        el.mozRequestFullScreen;
      rfs.call(el);
    });
  },
};
</script>
