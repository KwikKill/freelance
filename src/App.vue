<template>
  <div class="min-h-screen bg-gray-900 text-white w-full overflow-hidden">
    <!-- Animated Background Elements -->
    <div class="fixed inset-0 overflow-hidden pointer-events-none">
      <div class="floating-shapes">
        <div class="shape shape-1"></div>
        <div class="shape shape-2"></div>
        <div class="shape shape-3"></div>
        <div class="shape shape-4"></div>
        <div class="shape shape-5"></div>
      </div>
    </div>

    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-gray-900/95 backdrop-blur-sm z-50 border-b border-gray-800 py-4 px-6 flex items-center justify-between nav-slide-down">
      <div class="flex flex-row items-center gap-4">
        <div class="logo-container">
          <img src="@/assets/icon.png" alt="Logo" class="h-10 w-10 rounded-full logo-spin">
        </div>
        <div class="text-xl font-bold text-cyan-400 glow-text">Gabriel Blaisot</div>
      </div>
      <div class="hidden md:flex flex-1 justify-end gap-4">
        <a href="#services" class="nav-link">Services</a>
        <span class="text-gray-600">|</span>
        <a href="#portfolio" class="nav-link">Créations</a>
        <span class="text-gray-600">|</span>
        <a href="#about" class="nav-link">À propos</a>
        <span class="text-gray-600">|</span>
        <a href="#contact" class="nav-link">Contact</a>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
      <!-- Enhanced Background Pattern -->
      <div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-purple-900/20 to-cyan-900/20"></div>
      <div class="absolute inset-0 opacity-20">
        <div class="orb orb-1"></div>
        <div class="orb orb-2"></div>
        <div class="orb orb-3"></div>
      </div>

      <!-- Grid Pattern -->
      <div class="absolute inset-0 opacity-10">
        <div class="grid-pattern"></div>
      </div>

      <div class="relative z-10 text-center px-6 max-w-4xl mx-auto flex flex-col items-center gap-6 hero-content">
        <h1 class="text-5xl md:text-7xl font-bold mb-6 hero-title">
          <span class="gradient-text-animated">Création de sites web</span>
          <br>
          <span class="gradient-text-animated delay-300">professionnels</span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-4xl mx-auto hero-subtitle">
          Sites vitrines, e-commerce WordPress & développements sur mesure
        </p>
        <button
          @click="scrollToContact"
          class="cta-button"
        >
          <span class="button-text">Demander un devis</span>
          <div class="button-bg"></div>
          <div class="button-glow"></div>
        </button>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-20 px-6 m-12 flex flex-col items-center gap-12">
      <h2
        class="text-4xl font-bold text-center mb-16 section-title"
        data-aos="fade-up"
        data-aos-duration="1000"
      >
        Mes Services
      </h2>
      <div class="grid md:grid-cols-3 gap-8 services-grid">
        <!-- Site Vitrine -->
        <div
          class="service-card card-cyan"
          data-tilt
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="800"
        >
          <div class="card-inner">
            <div class="card-glow"></div>
            <div class="flex flex-row items-center justify-center gap-4">
              <div
                class="service-icon"
                data-aos="zoom-in"
                data-aos-delay="300"
                data-aos-duration="600"
              >🌐</div>
              <h3
                class="text-2xl font-bold mb-4 text-cyan-400"
                data-aos="fade-right"
                data-aos-delay="400"
              >Site Vitrine</h3>
            </div>
            <div
              class="price-tag"
              data-aos="fade-left"
              data-aos-delay="500"
            >
              À partir de <span class="price-highlight cyan">300€</span>
            </div>
            <p
              class="text-gray-300 mb-6"
              data-aos="fade-up"
              data-aos-delay="600"
            >
              Parfait pour les petites entreprises souhaitant une présence en ligne professionnelle et moderne.
            </p>
            <ul class="feature-list">
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="700"
              >✓ Design responsive</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="750"
              >✓ Optimisation SEO</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="800"
              >✓ Installation & configuration</li>
            </ul>
            <div
              class="flex justify-center"
              data-aos="zoom-in"
              data-aos-delay="900"
            >
              <button class="service-button cyan" @click="scrollToContact">
                <span>Demander un devis</span>
                <div class="button-ripple"></div>
              </button>
            </div>
          </div>
        </div>

        <!-- E-commerce -->
        <div
          class="service-card card-purple"
          data-tilt
          data-aos="fade-up"
          data-aos-delay="200"
          data-aos-duration="800"
        >
          <div class="card-inner">
            <div class="card-glow"></div>
            <div class="flex flex-row items-center justify-center gap-4">
              <div
                class="service-icon"
                data-aos="zoom-in"
                data-aos-delay="400"
                data-aos-duration="600"
              >🛒</div>
              <h3
                class="text-2xl font-bold mb-4 text-purple-400"
                data-aos="fade-right"
                data-aos-delay="500"
              >Site E-commerce</h3>
            </div>
            <div
              class="price-tag"
              data-aos="fade-left"
              data-aos-delay="600"
            >
              À partir de <span class="price-highlight purple">650€</span>
            </div>
            <p
              class="text-gray-300 mb-6"
              data-aos="fade-up"
              data-aos-delay="700"
            >
              Solution WooCommerce complète pour vendre vos produits en ligne efficacement.
            </p>
            <ul class="feature-list">
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="800"
              >✓ Catalogue de produits</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="850"
              >✓ Paiement sécurisé</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="900"
              >✓ Gestion des stocks</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="950"
              >✓ Formation incluse</li>
            </ul>
            <div
              class="flex justify-center"
              data-aos="zoom-in"
              data-aos-delay="1000"
            >
              <button class="service-button purple" @click="scrollToContact">
                <span>Demander un devis</span>
                <div class="button-ripple"></div>
              </button>
            </div>
          </div>
        </div>

        <!-- Sur mesure -->
        <div
          class="service-card card-pink"
          data-tilt
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="800"
        >
          <div class="card-inner">
            <div class="card-glow"></div>
            <div class="flex flex-row items-center justify-center gap-4">
              <div
                class="service-icon"
                data-aos="zoom-in"
                data-aos-delay="500"
                data-aos-duration="600"
              >⚡</div>
              <h3
                class="text-2xl font-bold mb-4 text-pink-400"
                data-aos="fade-right"
                data-aos-delay="600"
              >Site sur mesure</h3>
            </div>
            <div
              class="price-tag"
              data-aos="fade-left"
              data-aos-delay="700"
            >
              <span class="price-highlight pink">Sur devis</span>
            </div>
            <p
              class="text-gray-300 mb-6"
              data-aos="fade-up"
              data-aos-delay="800"
            >
              Développement personnalisé pour des besoins complexes et des fonctionnalités avancées.
            </p>
            <ul class="feature-list">
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="900"
              >✓ Frontend React / Vue.js</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="950"
              >✓ Backend adapté</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="1000"
              >✓ UI/UX sur mesure</li>
              <li
                class="feature-item"
                data-aos="slide-right"
                data-aos-delay="1050"
              >✓ Support technique</li>
            </ul>
            <div
              class="flex justify-center"
              data-aos="zoom-in"
              data-aos-delay="1100"
            >
              <button class="service-button pink" @click="scrollToContact">
                <span>Demander un devis</span>
                <div class="button-ripple"></div>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="py-20 px-6 bg-gray-800/30 flex flex-col items-center gap-12">
      <h2
        class="text-4xl font-bold text-center mb-16 section-title"
        data-aos="fade-down"
        data-aos-duration="1000"
      >
        Mes créations
      </h2>
      <div
        class="grid md:grid-cols-2 lg:grid-cols-3 gap-8"
      >
        <div
          v-for="project in projects"
          :key="project.id"
          @click="openModal(project)"
          class="bg-gray-800/50 rounded-2xl overflow-hidden border border-gray-700 hover:border-cyan-500/50 transition-all duration-300 cursor-pointer hover:transform hover:scale-105"
        >
          <div class="aspect-video bg-gradient-to-br from-cyan-500/20 to-purple-500/20 flex items-center justify-center overflow-hidden">
            <img
              :src="`${project.image}`"
              alt="Project Image"
              class="w-full h-auto object-cover"
              data-aos="zoom-in"
              data-aos-delay="100"
            />
          </div>
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2 text-cyan-400">{{ project.title }}</h3>
            <p class="text-gray-300 mb-4">{{ project.description }}</p>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="tech in project.stack"
                :key="tech"
                class="bg-gray-700 text-xs px-2 py-1 rounded-full text-gray-300"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
      <!--div
        class="text-center text-gray-400 portfolio-placeholder"
        data-aos="zoom-in"
        data-aos-delay="200"
        data-aos-duration="800"
      >
        <div
          class="placeholder-icon"
          data-aos="flip-up"
          data-aos-delay="400"
        >🚧</div>
        <p
          class="text-lg mb-2"
          data-aos="fade-up"
          data-aos-delay="600"
        >Je n'ai pas encore de projets professionnels à présenter.</p>
        <p
          data-aos="fade-up"
          data-aos-delay="700"
        >Revenez bientôt pour découvrir mes réalisations !</p>
      </div-->
      <div
        class="text-center mt-12"
        data-aos="slide-up"
        data-aos-delay="800"
      >
        <a
          href="https://gabriel.blaisot.org/?lang=fr&version=cyberpunk&theme=default#projects"
          class="portfolio-link"
          data-aos="pulse"
          data-aos-delay="1000"
        >
          <span>Voir mes projets personnels</span>
          <div class="link-arrow">→</div>
        </a>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-6 flex md:flex-row flex-col items-center gap-12 justify-center">
      <div
        class="about-image-container hidden md:block"
        data-aos="slide-right"
        data-aos-duration="1000"
        data-aos-offset="200"
      >
        <div class="image-frame">
          <img
            src="@/assets/icon.png"
            alt="Avatar de Gabriel Blaisot"
            class="about-image"
            data-aos="zoom-in"
            data-aos-delay="300"
          >
          <div class="image-glow"></div>
        </div>
      </div>
      <div class="max-w-4xl flex flex-col items-start gap-4 about-content">
        <h2
          class="text-4xl font-bold mb-6 section-title"
          data-aos="slide-left"
          data-aos-duration="800"
        >
          À propos de Moi
        </h2>
        <div class="about-text">
          <p
            class="text-gray-300 mb-6 leading-relaxed paragraph-slide"
            data-aos="fade-up"
            data-aos-delay="200"
            data-aos-duration="800"
          >
            Développeur web freelance passionné, je me spécialise dans la création de sites web modernes et performants.
            Avec une expertise en React et Vue.js, je porte une attention particulière à l'expérience utilisateur et au design.
          </p>
          <p
            class="text-gray-300 mb-8 leading-relaxed paragraph-slide"
            data-aos="fade-up"
            data-aos-delay="400"
            data-aos-duration="800"
          >
            Disponible pour vos projets, je vous accompagne de la conception à la mise en ligne,
            en passant par le développement et l'optimisation de votre présence digitale.
          </p>
        </div>
        <div
          class="flex flex-col md:flex-row items-center gap-4 mt-6 justify-center md:justify-start w-full md:w-auto about-buttons"
          data-aos="slide-up"
          data-aos-delay="600"
          data-aos-duration="600"
        >
          <a
            href="https://gabriel.blaisot.org/"
            target="_blank"
            rel="noopener noreferrer"
            class="about-button primary"
            data-aos="zoom-in"
            data-aos-delay="800"
          >
            <span>Voir mon portfolio</span>
            <div class="button-shine"></div>
          </a>
          <a
            href="/CV-Gabriel-Blaisot.pdf"
            target="_blank"
            rel="noopener noreferrer"
            class="about-button secondary"
            data-aos="zoom-in"
            data-aos-delay="900"
          >
            <span>Télécharger mon CV</span>
            <div class="button-shine"></div>
          </a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-6 bg-gray-800/30 flex flex-col items-center gap-12">
      <h2
        class="text-4xl font-bold text-center mb-16 section-title"
        data-aos="fade-down"
        data-aos-duration="1000"
      >
        Contactez-moi !
      </h2>
      <div class="max-w-4xl w-full flex-1 flex flex-col md:flex-row items-start md:items-center justify-between gap-12">
        <div
          class="w-full contact-form-container"
          data-aos="slide-right"
          data-aos-duration="800"
          data-aos-offset="100"
        >
          <form action="https://formspree.io/f/meogbwkq" method="POST" class="contact-form">
            <div
              class="form-group"
              data-aos="fade-up"
              data-aos-delay="100"
            >
              <label
                class="form-label"
                for="name"
              >
                Nom *
              </label>
              <input
                id="name"
                v-model="form.name"
                type="text"
                required
                name="name"
                class="form-input"
              >
              <div class="input-glow"></div>
            </div>
            <div
              class="form-group"
              data-aos="fade-up"
              data-aos-delay="200"
            >
              <label
                class="form-label"
                for="email"
              >
                Email *
              </label>
              <input
                id="email"
                v-model="form.email"
                type="email"
                required
                name="email"
                class="form-input"
              >
              <div class="input-glow"></div>
            </div>
            <div
              class="form-group"
              data-aos="fade-up"
              data-aos-delay="300"
            >
              <label
                class="form-label"
                for="projectType"
              >
                Type de projet
              </label>
              <select
                id="projectType"
                v-model="form.projectType"
                name="projectType"
                class="form-input"
              >
                <option value="">Sélectionnez un type</option>
                <option value="vitrine">Site Vitrine</option>
                <option value="ecommerce">E-commerce</option>
                <option value="custom">Sur mesure</option>
              </select>
              <div class="input-glow"></div>
            </div>
            <div
              class="form-group"
              data-aos="fade-up"
              data-aos-delay="400"
            >
              <label
                class="form-label"
                for="message"
              >
                Message *
              </label>
              <textarea
                id="message"
                v-model="form.message"
                required
                rows="5"
                name="message"
                class="form-input"
              />
              <div class="input-glow"></div>
            </div>
            <button
              type="submit"
              class="submit-button"
              data-aos="zoom-in"
              data-aos-delay="500"
              data-aos-duration="600"
            >
              <span class="button-text">Envoyer le message</span>
              <div class="button-bg"></div>
              <div class="submit-glow"></div>
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer
      class="py-12 px-6 border-t border-gray-800 flex flex-col items-center"
      data-aos="fade-up"
      data-aos-duration="800"
      data-aos-offset="50"
    >
      <div class="flex flex-col md:flex-row justify-center items-center">
        <div class="mb-4 md:mb-0">
          <p class="text-gray-400">© {{ new Date().getFullYear() }} Gabriel Blaisot. Tous droits réservés.</p>
        </div>
      </div>
    </footer>

    <!-- Modal -->
    <div
      v-if="selectedProject"
      @click="closeModal"
      class="modal-overlay"
    >
      <div
        @click.stop
        class="modal-content flex flex-col gap-2"
      >
        <div class="flex justify-between items-start mb-6">
          <h3 class="text-2xl font-bold text-cyan-400">{{ selectedProject.title }}</h3>
          <button @click="closeModal" class="modal-close">×</button>
        </div>
        <div class="modal-image border border-gray-700 rounded-lg overflow-hidden mb-6">
          <img
            :src="`${selectedProject.image}`"
            alt="Project Image"
            class="w-full h-auto object-cover rounded-lg"
          />
        </div>
        <p class="text-gray-300 mb-6">{{ selectedProject.fullDescription }}</p>
        <div class="flex flex-wrap gap-2 mb-6">
          <span
            v-for="tech in selectedProject.stack"
            :key="tech"
            class="tech-tag"
          >
            {{ tech }}
          </span>
        </div>
        <div class="flex gap-4">
          <a
            class="modal-button primary"
            :href="selectedProject.link"
            target="_blank"
            rel="noopener noreferrer"
          >
            Voir le site
        </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive, onMounted, onUnmounted } from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
import esport from '@/assets/projects/esportrecrutement.webp';

// Initialize AOS on component mount
onMounted(() => {
  AOS.init({
    duration: 800,
    easing: 'ease-out-cubic',
    once: true,
    offset: 100,
    delay: 0,
    anchorPlacement: 'top-bottom'
  })
})

onUnmounted(() => {
  AOS.refresh()
})

// Form data
const form = reactive({
  name: '',
  email: '',
  projectType: '',
  message: ''
})

// Portfolio projects
const projects = ref([
  {
    id: 1,
    title: 'EsportRecrutement.fr',
    description: 'SaaS de recrutement esports',
    fullDescription: 'EsportRecrutement.fr est un site dédié au recrutement de joueurs esports.Il permet aux joueurs de créer des profils dans l\'annuaire, rechercher des équipes et de postuler à des postes dans diverses équipes esports. Le site inclus un système d\'annonces, de blog, de chat entre utilisteurs, de paiement et un panel admin complet.',
    stack: ['Next.js', 'React', 'HTML', 'CSS', 'Tailwind CSS', 'TypeScript'],
    image: esport,
    link: "https://esportrecrutement.fr"
  },
])

// Modal state
const selectedProject = ref(null)

// Methods
const scrollToContact = () => {
  document.getElementById('contact').scrollIntoView({ behavior: 'smooth' })
}

const openModal = (project) => {
  selectedProject.value = project
}

const closeModal = () => {
  selectedProject.value = null
}
</script>

<style scoped>
/* Base Styles */
html {
  scroll-behavior: smooth;
}

/* Floating Background Shapes */
.floating-shapes {
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.shape {
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(45deg, rgba(6, 182, 212, 0.1), rgba(168, 85, 247, 0.1));
  animation: float 20s infinite linear;
}

.shape-1 {
  width: 80px;
  height: 80px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 120px;
  height: 120px;
  top: 60%;
  right: 10%;
  animation-delay: -5s;
}

.shape-3 {
  width: 60px;
  height: 60px;
  top: 80%;
  left: 20%;
  animation-delay: -10s;
}

.shape-4 {
  width: 100px;
  height: 100px;
  top: 30%;
  right: 30%;
  animation-delay: -15s;
}

.shape-5 {
  width: 40px;
  height: 40px;
  top: 10%;
  right: 50%;
  animation-delay: -7s;
}

@keyframes float {
  0% {
    transform: translateY(0px) rotate(0deg);
    opacity: 0.7;
  }
  33% {
    transform: translateY(-30px) rotate(120deg);
    opacity: 0.4;
  }
  66% {
    transform: translateY(30px) rotate(240deg);
    opacity: 0.7;
  }
  100% {
    transform: translateY(0px) rotate(360deg);
    opacity: 0.7;
  }
}

/* Navigation Animations */
.nav-slide-down {
  animation: slideDown 0.8s ease-out;
}

@keyframes slideDown {
  from {
    transform: translateY(-100%);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

.logo-container {
  position: relative;
  overflow: hidden;
  border-radius: 50%;
}

.logo-spin {
  transition: transform 0.6s ease;
}

.logo-container:hover .logo-spin {
  transform: rotate(360deg) scale(1.1);
}

.glow-text {
  text-shadow: 0 0 10px rgba(6, 182, 212, 0.5);
  animation: textGlow 2s ease-in-out infinite alternate;
}

@keyframes textGlow {
  from {
    text-shadow: 0 0 10px rgba(6, 182, 212, 0.5);
  }
  to {
    text-shadow: 0 0 20px rgba(6, 182, 212, 0.8), 0 0 30px rgba(6, 182, 212, 0.6);
  }
}

.nav-link {
  position: relative;
  color: #d1d5db;
  transition: color 0.3s ease;
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  overflow: hidden;
}

.nav-link::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(6, 182, 212, 0.2), transparent);
  transition: left 0.5s ease;
}

.nav-link:hover::before {
  left: 100%;
}

.nav-link:hover {
  color: #06b6d4;
}

/* Hero Section Animations */
.hero-content {
  animation: heroFadeIn 1.2s ease-out;
}

@keyframes heroFadeIn {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-title {
  animation: titleSlideUp 1s ease-out 0.3s both;
}

.hero-subtitle {
  animation: titleSlideUp 1s ease-out 0.6s both;
}

@keyframes titleSlideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.gradient-text-animated {
  background: linear-gradient(45deg, #06b6d4, #8b5cf6, #ec4899, #06b6d4);
  background-size: 300% 300%;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientShift 4s ease-in-out infinite;
}

.delay-300 {
  animation-delay: 0.3s;
}

@keyframes gradientShift {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

/* Enhanced Orbs */
.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(40px);
  animation: orbFloat 8s ease-in-out infinite;
}

.orb-1 {
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.4), transparent);
  top: 20%;
  left: 20%;
  animation-delay: 0s;
}

.orb-2 {
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(168, 85, 247, 0.3), transparent);
  top: 40%;
  right: 20%;
  animation-delay: -2s;
}

.orb-3 {
  width: 250px;
  height: 250px;
  background: radial-gradient(circle, rgba(236, 72, 153, 0.3), transparent);
  bottom: 20%;
  left: 50%;
  animation-delay: -4s;
}

@keyframes orbFloat {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  33% {
    transform: translate(30px, -30px) scale(1.1);
  }
  66% {
    transform: translate(-20px, 20px) scale(0.9);
  }
}

/* Grid Pattern */
.grid-pattern {
  width: 100%;
  height: 100%;
  background-image:
    linear-gradient(rgba(6, 182, 212, 0.1) 1px, transparent 1px),
    linear-gradient(90deg, rgba(6, 182, 212, 0.1) 1px, transparent 1px);
  background-size: 50px 50px;
  animation: gridMove 20s linear infinite;
}

@keyframes gridMove {
  0% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(50px, 50px);
  }
}

/* CTA Button */
.cta-button {
  position: relative;
  padding: 1rem 2rem;
  border: none;
  border-radius: 9999px;
  font-weight: bold;
  font-size: 1.125rem;
  cursor: pointer;
  overflow: hidden;
  transition: transform 0.3s ease;
  animation: buttonPulse 2s ease-in-out infinite;
}

.cta-button:hover {
  transform: scale(1.05);
}

.button-text {
  position: relative;
  z-index: 3;
  color: white;
}

.button-bg {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6);
  z-index: 1;
}

.button-glow {
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6, #ec4899, #06b6d4);
  background-size: 300% 300%;
  border-radius: 9999px;
  z-index: 0;
  animation: buttonGlow 3s ease-in-out infinite;
}

@keyframes buttonPulse {
  0%, 100% {
    box-shadow: 0 0 20px rgba(6, 182, 212, 0.4);
  }
  50% {
    box-shadow: 0 0 40px rgba(6, 182, 212, 0.8), 0 0 60px rgba(168, 85, 247, 0.4);
  }
}

@keyframes buttonGlow {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

/* Section Animations */
.section-fade-in {
  animation: sectionFadeIn 1s ease-out;
}

@keyframes sectionFadeIn {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.section-title {
  background: linear-gradient(45deg, #06b6d4, #8b5cf6);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  position: relative;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 3px;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6);
  border-radius: 2px;
}

/* Service Cards */
.services-grid {
  animation: gridFadeIn 1.2s ease-out 0.3s both;
}

@keyframes gridFadeIn {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.service-card {
  position: relative;
  background: rgba(31, 41, 55, 0.5);
  backdrop-filter: blur(10px);
  border-radius: 1rem;
  padding: 2rem;
  border: 1px solid rgba(75, 85, 99, 0.5);
  transition: all 0.4s ease;
  overflow: hidden;
  cursor: pointer;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  transition: left 0.6s ease;
}

.service-card:hover::before {
  left: 100%;
}

.service-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.card-cyan:hover {
  border-color: rgba(6, 182, 212, 0.5);
  box-shadow: 0 20px 40px rgba(6, 182, 212, 0.2);
}

.card-purple:hover {
  border-color: rgba(168, 85, 247, 0.5);
  box-shadow: 0 20px 40px rgba(168, 85, 247, 0.2);
}

.card-pink:hover {
  border-color: rgba(236, 72, 153, 0.5);
  box-shadow: 0 20px 40px rgba(236, 72, 153, 0.2);
}

.card-inner {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.card-glow {
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.1), transparent);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.service-card:hover .card-glow {
  opacity: 1;
}

.service-icon {
  font-size: 3rem;
  text-align: center;
  animation: iconBounce 2s ease-in-out infinite;
}

@keyframes iconBounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

.price-tag {
  font-size: 1.875rem;
  font-weight: bold;
  margin-bottom: 1rem;
  text-align: center;
}

.price-highlight {
  position: relative;
  padding: 0.25rem 0.5rem;
  border-radius: 0.5rem;
}

.price-highlight.cyan {
  color: #06b6d4;
  background: rgba(6, 182, 212, 0.1);
}

.price-highlight.purple {
  color: #8b5cf6;
  background: rgba(139, 92, 246, 0.1);
}

.price-highlight.pink {
  color: #ec4899;
  background: rgba(236, 72, 153, 0.1);
}

.feature-list {
  list-style: none;
  padding: 0;
  margin-bottom: 2rem;
}

.feature-item {
  color: #d1d5db;
  margin-bottom: 0.5rem;
  opacity: 0;
  animation: featureSlideIn 0.6s ease-out forwards;
}

.feature-item:nth-child(1) { animation-delay: 0.1s; }
.feature-item:nth-child(2) { animation-delay: 0.2s; }
.feature-item:nth-child(3) { animation-delay: 0.3s; }
.feature-item:nth-child(4) { animation-delay: 0.4s; }

@keyframes featureSlideIn {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.service-button {
  position: relative;
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 0.5rem;
  font-weight: bold;
  cursor: pointer;
  overflow: hidden;
  transition: all 0.3s ease;
}

.service-button.cyan {
  background: #0891b2;
  color: white;
}

.service-button.purple {
  background: #7c3aed;
  color: white;
}

.service-button.pink {
  background: #db2777;
  color: white;
  font-weight: bold;
}

.service-button:hover {
  transform: translateY(-2px);
}

.button-ripple {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: width 0.6s ease, height 0.6s ease;
}

.service-button:active .button-ripple {
  width: 300px;
  height: 300px;
}

/* Portfolio Section */
.portfolio-placeholder {
  animation: placeholderFadeIn 1s ease-out 0.5s both;
}

@keyframes placeholderFadeIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.placeholder-icon {
  font-size: 4rem;
  margin-bottom: 1rem;
  animation: iconRotate 3s ease-in-out infinite;
}

@keyframes iconRotate {
  0%, 100% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(10deg);
  }
}

.portfolio-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: #06b6d4;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
  padding: 0.75rem 1.5rem;
  border: 1px solid rgba(6, 182, 212, 0.3);
  background: rgba(6, 182, 212, 0.05);
}

.portfolio-link:hover {
  color: #0891b2;
  border-color: rgba(6, 182, 212, 0.6);
  background: rgba(6, 182, 212, 0.1);
}

.link-arrow {
  transition: transform 0.3s ease;
}

.portfolio-link:hover .link-arrow {
  transform: translateX(5px);
}

/* About Section */
.about-image-container {
  animation: imageSlideIn 1s ease-out 0.3s both;
}

@keyframes imageSlideIn {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.image-frame {
  position: relative;
  width: 320px;
  height: 320px;
  background: linear-gradient(45deg, rgba(6, 182, 212, 0.2), rgba(168, 85, 247, 0.2));
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(75, 85, 99, 0.5);
  overflow: hidden;
}

.image-frame::before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6, #ec4899, #06b6d4);
  background-size: 300% 300%;
  border-radius: 1rem;
  z-index: -1;
  animation: borderGlow 4s ease-in-out infinite;
}

@keyframes borderGlow {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

.about-image {
  width: 256px;
  height: 256px;
  border-radius: 50%;
  object-fit: cover;
  transition: transform 0.4s ease;
  padding: 0.5rem;
}

.image-frame:hover .about-image {
  transform: scale(1.05);
}

.image-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 250px;
  height: 250px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.3), transparent);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.image-frame:hover .image-glow {
  opacity: 1;
}

.about-content {
  animation: contentSlideIn 1s ease-out 0.6s both;
}

@keyframes contentSlideIn {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.paragraph-slide {
  animation: paragraphFadeIn 0.8s ease-out both;
}

.paragraph-slide:nth-child(1) { animation-delay: 0.2s; }
.paragraph-slide:nth-child(2) { animation-delay: 0.4s; }

@keyframes paragraphFadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.about-buttons {
  animation: buttonsSlideUp 1s ease-out 0.8s both;
}

@keyframes buttonsSlideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.about-button {
  position: relative;
  display: inline-flex;
  align-items: center;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  font-weight: bold;
  text-decoration: none;
  transition: all 0.3s ease;
  overflow: hidden;
}

.about-button.primary {
  background: #374151;
  color: white;
  border: 1px solid #4b5563;
}

.about-button.secondary {
  background: #374151;
  color: white;
  border: 1px solid #4b5563;
}

.about-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.about-button.primary:hover {
  background: #4b5563;
  border-color: #06b6d4;
}

.about-button.secondary:hover {
  background: #4b5563;
  border-color: #8b5cf6;
}

.button-shine {
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.6s ease;
}

.about-button:hover .button-shine {
  left: 100%;
}

/* Contact Form */
.contact-form-container {
  animation: formSlideIn 1s ease-out 0.4s both;
}

@keyframes formSlideIn {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group {
  position: relative;
}

.form-label {
  display: block;
  color: #d1d5db;
  margin-bottom: 0.5rem;
  font-weight: 500;
}

.form-input {
  width: 100%;
  background: rgba(31, 41, 55, 0.8);
  border: 1px solid #374151;
  border-radius: 0.5rem;
  padding: 0.75rem 1rem;
  color: white;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.form-input:focus {
  outline: none;
  border-color: #06b6d4;
  box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.1);
}

.input-glow {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 0.5rem;
  background: linear-gradient(45deg, transparent, rgba(6, 182, 212, 0.1), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
  pointer-events: none;
}

.form-input:focus + .input-glow {
  opacity: 1;
}

.submit-button {
  position: relative;
  width: 100%;
  padding: 1rem 1.5rem;
  border: none;
  border-radius: 0.5rem;
  font-weight: bold;
  cursor: pointer;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.submit-button:hover {
  transform: translateY(-2px);
}

.submit-button .button-text {
  position: relative;
  z-index: 3;
  color: white;
}

.submit-button .button-bg {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6);
  z-index: 1;
}

.submit-glow {
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, #06b6d4, #8b5cf6, #ec4899, #06b6d4);
  background-size: 300% 300%;
  animation: submitGlow 3s ease-in-out infinite;
}

@keyframes submitGlow {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

/* Footer */
.footer-fade-in {
  animation: footerFadeIn 1s ease-out 0.6s both;
}

@keyframes footerFadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Modal */
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(10px);
  z-index: 50;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  animation: modalFadeIn 0.3s ease-out;
}

@keyframes modalFadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.modal-content {
  background: #1f2937;
  border-radius: 1rem;
  padding: 2rem;
  max-width: 32rem;
  width: 100%;
  border: 1px solid #374151;
  animation: modalSlideIn 0.4s ease-out;
}

@keyframes modalSlideIn {
  from {
    opacity: 0;
    transform: scale(0.9) translateY(20px);
  }
  to {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

.modal-close {
  background: none;
  border: none;
  color: #9ca3af;
  font-size: 1.5rem;
  cursor: pointer;
  transition: color 0.3s ease;
}

.modal-close:hover {
  color: white;
}

.modal-image {
  height: 16rem;
  background: linear-gradient(45deg, rgba(6, 182, 212, 0.2), rgba(168, 85, 247, 0.2));
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.tech-tag {
  background: #374151;
  font-size: 0.875rem;
  padding: 0.25rem 0.75rem;
  border-radius: 9999px;
  color: #d1d5db;
}

.modal-button {
  padding: 0.5rem 1.5rem;
  border-radius: 0.5rem;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
}

.modal-button.primary {
  background: #0891b2;
  color: white;
  border: none;
}

.modal-button.secondary {
  background: #374151;
  color: white;
  border: 1px solid #4b5563;
}

.modal-button:hover {
  transform: translateY(-1px);
}

/* Custom Scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1f2937;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(45deg, #06b6d4, #8b5cf6);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(45deg, #0891b2, #7c3aed);
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }

  .hero-subtitle {
    font-size: 1.125rem;
  }

  .service-card {
    margin-bottom: 1rem;
  }

  .about-image-container {
    display: none;
  }

  .shape {
    display: none;
  }
}

/* Performance Optimizations */
.service-card,
.about-button,
.form-input,
.cta-button {
  will-change: transform;
}

/* Accessibility */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

/* AOS Custom Animations */
[data-aos="slide-up"] {
  transform: translate3d(0, 40px, 0);
  opacity: 0;
}

[data-aos="slide-up"].aos-animate {
  transform: translate3d(0, 0, 0);
  opacity: 1;
}

[data-aos="pulse"] {
  transform: scale(0.9);
  opacity: 0.7;
}

[data-aos="pulse"].aos-animate {
  transform: scale(1);
  opacity: 1;
}

[data-aos="flip-up"] {
  transform: perspective(400px) rotateX(90deg);
  opacity: 0;
}

[data-aos="flip-up"].aos-animate {
  transform: perspective(400px) rotateX(0deg);
  opacity: 1;
}

/* Enhanced AOS transitions */
.aos-init[data-aos] {
  transition-property: transform, opacity;
  transition-timing-function: cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Remove old animation classes that conflict with AOS */
.section-fade-in,
.services-grid,
.contact-form-container,
.about-image-container,
.about-content,
.footer-fade-in {
  /* Remove old animations, AOS handles these now */
}
</style>
