<template>
    <section class="container my-5" id="tech">
      <h2>Tech Stack</h2>
      <div class="row">
        <div class="col-md-4" v-for="skill in tech" :key="skill.id">
          <div class="card mb-3">
            <div class="card-body">
              <h5 class="card-title">{{ skill.name }}</h5>
              <p class="card-text">{{ skill.level }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Tech',
    data() {
      return {
        tech: [
        {id: 1, name: 'Docker'},
        {id: 2, name: 'Cpanel'},
        {id: 3, name: 'Nginx'},
        {id: 4, name: 'Portainer'},
        {id: 5, name: 'Wordpress'},
        {id: 6, name: 'Git'},
          // Tambahkan skill lainnya di sini
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  #tech h5 {
    text-align: center;
  }
  </style>