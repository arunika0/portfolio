<template>
  <div>
    <header class="name text-center bg-primary text-white py-5">
      <nav>
        <ul class="nav-menu">
          <li><a href="#about" class="text-white mx-2">About</a></li>
          <li><a href="#experience" class="text-white mx-2">Experience</a></li>
          <li><a href="#education" class="text-white mx-2">Education</a></li>
          <li><a href="#tech" class="text-white mx-2">Tech Stack</a></li>
        </ul>
        <h1>CAKRA PRADIPTA KUNTARA</h1>
        <p>D3 Brawijaya University</p>
        <a href="https://github.com" class="text-white mx-2"><i class="fab fa-github"></i></a>
        <a href="https://linkedin.com" class="text-white mx-2"><i class="fab fa-linkedin"></i></a>
      </nav>
    </header>
    <About />
    <Experience />
    <Education />
    <Skills />
    <button v-show="showBackToTop" class="back-to-top" @click="scrollToTop">Kembali ke Atas</button>
  </div>
</template>

<script>
import Projects from '~/components/Projects.vue';
import Skills from '~/components/Skills.vue';

export default {
  components: {
    About: () => import('@/components/About.vue'),
    Experience: () => import('@/components/Experience.vue'),
    Education: () => import('@/components/Education.vue'),
    Skills: () => import('@/components/Skills.vue'),
  },
  data() {
    return {
      showBackToTop: false
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    },
    handleScroll() {
      this.showBackToTop = window.scrollY > 200;
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  }
};
</script>

<style scoped>
.name {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.nav-menu {
  list-style: none;
  padding: 0;
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.nav-menu li {
  margin: 0 10px;
}

.nav-menu a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.back-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

.back-to-top:hover {
  background-color: #0056b3;
}
</style>
