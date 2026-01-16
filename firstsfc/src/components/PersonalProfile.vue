<template>
  <div :class="{ 'dark-theme': isDark }" id="page-body">
    <nav class="navbar navbar-expand-lg navbar-dark custom-nav shadow-sm sticky-top">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#">JPCABIGAN</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarMenu">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarMenu">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link px-3" href="#education">Education</a></li>
            <li class="nav-item"><a class="nav-link px-3" href="#interests">Interests</a></li>
            <li class="nav-item"><a class="nav-link px-3" href="#gallery">Anime</a></li>
            <li class="nav-item"><a class="nav-link px-3" href="#resources">Resources</a></li>
            <li class="nav-item px-2">
              <button @click="toggleTheme" class="btn btn-dark btn-sm fw-bold">See Some Magic</button>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <header class="hero-header text-center py-5">
      <div class="container">
        <img src="https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/adg.png?raw=true" class="profile-circle mb-3 shadow" alt="Profile">
        <h1 class="display-5 fw-bold">John Patrick Cabigan</h1>
        <p class="lead">Section IT242 • Silly Energetic Human</p>
        <p class="mt-4 px-3 description-text">
          I’m a 5'10 ft tall that was born in Donsol, Sorsogon, a manga collector, and an airplane enthusiast who loves commercial airliners. 
          I enjoy bonding with friends, exploring new places, and learning creative digital hobbies.
        </p>
      </div>
    </header>

    <div class="container my-5">
      <div class="row gy-5">
        <div class="col-lg-6" id="education">
          <div class="info-card h-100">
            <h2 class="h4 gold-text border-bottom pb-2 mb-4">Academic History</h2>
            <div class="d-flex align-items-center mb-4">
              <img src="https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/ftjca-removebg-preview.png?raw=true" class="school-logo me-3" alt="FTJCA Logo">
              <div><strong>FTJCA</strong><br><small class="text-muted">Elementary</small></div>
            </div>
            <div class="d-flex align-items-center">
              <img src="https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/svnhs-removebg-preview.png?raw=true" class="school-logo me-3" alt="SVNHS Logo">
              <div><strong>SVNHS</strong><br><small class="text-muted">Junior & Senior High</small></div>
            </div>
          </div>
        </div>

        <div class="col-lg-6" id="interests">
          <div class="info-card h-100">
            <h2 class="h4 gold-text border-bottom pb-2 mb-4">Interests & Hobbies</h2>
            <p>✈️ <strong>Collections:</strong> Airplane models and Manga series</p>
            <p>🎬 <strong>Creativity:</strong> Cinema movies, Art Design, Photo Editing, Video Editing</p>
            <p>🤝 <strong>Social:</strong> Hanging out with friends</p>
          </div>
        </div>
      </div>

      <div class="row mt-5 pt-5 justify-content-center" id="gallery">
        <h2 class="text-center fw-bold mb-5 gold-text">Top 5 Favorite Anime</h2>
        <div class="col-md-4 col-sm-6 mb-4" v-for="anime in animeList" :key="anime.name">
          <div class="anime-card">
            <img :src="anime.url" :alt="anime.name">
            <div class="anime-overlay"><span>{{ anime.name }}</span></div>
          </div>
        </div>
      </div>

      <div class="row mt-5" id="resources">
        <div class="col-12">
          <div class="info-card">
            <h2 class="h4 gold-text border-bottom pb-2 mb-4">RESOURCES</h2>
            <div class="row gy-3">
              <div class="col-md-6">
                <p><strong>1. Gemini:</strong> AI partner for debugging.</p>
                <p><strong>2. W3Schools:</strong> Reference for CSS/HTML.</p>
                <p><strong>3. YouTube:</strong> Bootstrap tutorials.</p>
              </div>
              <div class="col-md-6">
                <p><strong>4. StartBootstrap:</strong> Bare Template foundation.</p>
                <p><strong>5. W3C Validator:</strong> Code error checking.</p>
                <p><strong>6. ResponsiveTestTool:</strong> Mobile verification.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PersonalProfile',
  data() {
    return {
      isDark: false,
      animeList: [
        { name: 'Violet Evergarden', url: 'https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/violet.jpg?raw=true' },
        { name: 'A Galaxy Next Door', url: 'https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/galaxy.jpg?raw=true' },
        { name: 'The Fragrant Flower Blooms with Dignity', url: 'https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/waguri.jpg?raw=true' },
        { name: 'Kimi no Todoke', url: 'https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/sawako.jpg?raw=true' },
        { name: 'The Wind Rises', url: 'https://github.com/PatrickCabigan/WEBPROG-IT242-HTML-LESSONS/blob/feature/2_JPC_customize_my_website/wind%20rises.jpg?raw=true' }
      ]
    };
  },
  methods: {
    toggleTheme() {
      this.isDark = !this.isDark;
    }
  }
};
</script>

<style scoped>
/* Importing your external CSS file */
@import "@/assets/css/PersonalProfile.css";
</style>