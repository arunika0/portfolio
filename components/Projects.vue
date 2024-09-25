<template>
    <section class="container my-5" id="projects">
        <h2>Projects</h2>
        <div class="card mb-3" v-for="project in projects" :key="project.id">
            <div class="card-body">
                <h5 class="card-title">{{ project.name }}</h5>
                <p class="text-muted">{{ project.description }}</p>
                <a :href="project.link" target="_blank" class="project-link">View Project</a>
            </div>
        </div>
    </section>
</template>
  
  <script>
  export default {
    name: 'Projects',
    data() {
      return {
        projects: [
          { id: 1, name: 'Project One', description: 'Description for project one', link: 'https://example.com/project-one' },
          { id: 2, name: 'Project Two', description: 'Description for project two', link: 'https://example.com/project-two' },
          // Tambahkan proyek lainnya di sini
        ]
      };
    }
  };
  </script>