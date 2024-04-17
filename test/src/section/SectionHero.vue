<template>
  <!-- HERO SECTION START -->
  <section class="hero-section d-flex align-items-center" id="intro">
    <div class="intro_text">
      <svg viewBox="0 0 1320 300">
        <text x="50%" Y="50%" text-anchor="middle">AMMAR</text>
      </svg>
    </div>
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md-6">
          <div class="hero-content-box">
            <span class="hero-sub-title">Muammar.</span>
            <h1 class="hero-title">{{ hero.role }}</h1>

            <div class="hero-image-box d-md-none text-center">
              <img :src="hero.image" alt="" />
            </div>

            <p class="lead">{{ hero.description }}</p>
            <div class="button-box d-flex flex-wrap align-items-center">
              <a href="#" class="btn tj-btn-secondary"
                >Download CV <i class="flaticon-download"></i
              ></a>
              <ul class="ul-reset social-icons">
                <li>
                  <a href="#"><i class="fa-brands fa-twitter"></i></a>
                </li>
                <li>
                  <a href="#"><i class="fa-light fa-basketball"></i></a>
                </li>
                <li>
                  <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                </li>
                <li>
                  <a href="#"><i class="fa-brands fa-github"></i></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-md-6 d-none d-md-block">
          <div class="hero-image-box text-center">
            <img :src="hero.image" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- HERO SECTION END -->
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      hero: {}
    }
  },
  created() {
    this.fetchHeroData()
  },
  methods: {
    async fetchHeroData() {
      try {
        const response = await axios.get('http://localhost:1337/api/hero?populate=*')
        this.hero = response.data.data.attributes
        this.hero.image = 'http://localhost:1337/uploads/muam_74aef96d7d.jpg'
      } catch (error) {
        console.error('Error fetching hero data:', error)
      }
    }
  }
}
</script>

<style>
/* Your CSS styles */
</style>
