<template>
  <div>
    <header class="text-center bg-primary text-white py-5">
      <h1>CAKRA PRADIPTA KUNTARA</h1>
      <p>D3 Brawijaya University</p>
      <a href="https://github.com" class="text-white mx-2"><i class="fab fa-github"></i></a>
      <a href="https://linkedin.com" class="text-white mx-2"><i class="fab fa-linkedin"></i></a>
    </header>

    <About />
    <Experience />
    <Education />
    <Projects />
  </div>
</template>

<script>
export default {
  components: {
    About: () => import('@/components/About.vue'),
    Experience: () => import('@/components/Experience.vue'),
    Education: () => import('@/components/Education.vue'),
  },
};
</script>

<style scoped>
header {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}
</style>
