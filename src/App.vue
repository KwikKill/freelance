<template>
  <div class="min-h-screen bg-gray-900 text-white w-full">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-gray-900/95 backdrop-blur-sm z-50 border-b border-gray-800 py-4 px-6 flex items-center justify-between">
      <div class="flex flex-row items-center gap-4">
        <img src="@/assets/icon.svg" alt="Logo" class="h-10 w-10 rounded-full">
        <div class="text-xl font-bold text-cyan-400">Gabriel Blaisot</div>
      </div>
      <div class="hidden md:flex flex-1 justify-end gap-4">
        <a href="#services" class="hover:text-cyan-400 transition-colors rounded-lg">Services</a>
        <p>
          |
        </p>
        <a href="#portfolio" class="hover:text-cyan-400 transition-colors rounded-lg">Créations</a>
        <p>
          |
        </p>
        <a href="#about" class="hover:text-cyan-400 transition-colors rounded-lg">À propos</a>
        <p>
          |
        </p>
        <a href="#contact" class="hover:text-cyan-400 transition-colors rounded-lg">Contact</a>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
      <!-- Background Pattern -->
      <div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-purple-900/20 to-cyan-900/20"></div>
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-20 left-20 w-72 h-72 bg-cyan-500 rounded-full mix-blend-multiply filter blur-xl animate-pulse"></div>
        <div class="absolute top-40 right-20 w-72 h-72 bg-purple-500 rounded-full mix-blend-multiply filter blur-xl animate-pulse delay-1000"></div>
        <div class="absolute bottom-20 left-1/2 w-72 h-72 bg-pink-500 rounded-full mix-blend-multiply filter blur-xl animate-pulse delay-2000"></div>
      </div>

      <div class="relative z-10 text-center px-6 max-w-4xl mx-auto flex flex-col items-center gap-6">
        <h1 class="text-5xl md:text-7xl font-bold mb-6 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">
          Création de sites web professionnels
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-4xl mx-auto">
          Sites vitrines, e-commerce WordPress & développements sur mesure
        </p>
        <button
          @click="scrollToContact"
          class="bg-gradient-to-r from-cyan-500 to-purple-500 hover:from-cyan-600 hover:to-purple-600 text-white font-bold py-4 px-8 rounded-full text-lg transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-cyan-500/25"
        >
          Demander un devis
        </button>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-20 px-6 m-12 flex flex-col items-center gap-12">
      <h2 class="text-4xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">
        Mes Services
      </h2>
      <div class="grid md:grid-cols-3 gap-8">
        <!-- Site Vitrine -->
        <div class="bg-gray-800/50 backdrop-blur-sm rounded-2xl p-8 border border-gray-700 hover:border-cyan-500/50 transition-all duration-300 hover:transform hover:scale-105 flex flex-col gap-2">
          <div class="flex flex-row items-center justify-center mb-4 gap-4">
            <div class="text-cyan-400 text-4xl mb-4">🌐</div>
            <h3 class="text-2xl font-bold mb-4 text-cyan-400">Site Vitrine</h3>
          </div>
          <div class="text-3xl font-bold mb-4">À partir de <span class="text-cyan-400">300€</span></div>
          <p class="text-gray-300 mb-6">
            Parfait pour les petites entreprises souhaitant une présence en ligne professionnelle et moderne.
          </p>
          <ul class="text-gray-400 space-y-2">
            <li>✓ Design responsive</li>
            <li>✓ Optimisation SEO</li>
            <li>✓ Installation & configuration</li>
          </ul>

          <div class="flex justify-center">
            <button
              class="mt-6 bg-cyan-600 hover:bg-cyan-700 text-white font-bold py-3 px-6 rounded-lg transition-colors cursor-pointer"
              @click="scrollToContact"
            >
              Demander un devis
          </button>
          </div>
        </div>

        <!-- E-commerce -->
        <div class="bg-gray-800/50 backdrop-blur-sm rounded-2xl p-8 border border-gray-700 hover:border-purple-500/50 transition-all duration-300 hover:transform hover:scale-105 flex flex-col gap-2">
          <div class="flex flex-row items-center justify-center mb-4 gap-4">
            <div class="text-purple-400 text-4xl mb-4">🛒</div>
            <h3 class="text-2xl font-bold mb-4 text-purple-400">Site E-commerce</h3>
          </div>
          <div class="text-3xl font-bold mb-4">À partir de <span class="text-purple-400">650€</span></div>
          <p class="text-gray-300 mb-6">
            Solution WooCommerce complète pour vendre vos produits en ligne efficacement.
          </p>
          <ul class="text-gray-400 space-y-2">
            <li>✓ Catalogue de produits</li>
            <li>✓ Paiement sécurisé</li>
            <li>✓ Gestion des stocks</li>
            <li>✓ Formation incluse</li>
          </ul>

          <div class="flex justify-center">
            <button
              class="mt-6 bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-6 rounded-lg transition-colors cursor-pointer"
              @click="scrollToContact"
            >
              Demander un devis
            </button>
          </div>
        </div>

        <!-- Sur mesure -->
        <div class="bg-gray-800/50 backdrop-blur-sm rounded-2xl p-8 border border-gray-700 hover:border-pink-500/50 transition-all duration-300 hover:transform hover:scale-105 flex flex-col gap-2">
          <div class="flex flex-row items-center justify-center mb-4 gap-4">
            <div class="text-pink-400 text-4xl mb-4">⚡</div>
            <h3 class="text-2xl font-bold mb-4 text-pink-400">Site sur mesure</h3>
          </div>
          <div class="text-3xl font-bold mb-4"><span class="text-pink-400">Sur devis</span></div>
          <p class="text-gray-300 mb-6">
            Développement personnalisé pour des besoins complexes et des fonctionnalités avancées.
          </p>
          <ul class="text-gray-400 space-y-2">
            <li>✓ Frontend React / Vue.js</li>
            <li>✓ Backend adapté</li>
            <li>✓ UI/UX sur mesure</li>
            <li>✓ Support technique</li>
          </ul>

          <div class="flex justify-center">
            <button
              class="mt-6 bg-pink-600 hover:bg-pink-700 text-white font-bold py-3 px-6 rounded-lg transition-colors cursor-pointer"
              @click="scrollToContact"
            >
              Demander un devis
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="py-20 px-6 bg-gray-800/30 flex flex-col items-center gap-12">
      <h2 class="text-4xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">
        Mes créations
      </h2>
      <!--div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="project in projects"
          :key="project.id"
          @click="openModal(project)"
          class="bg-gray-800/50 rounded-2xl overflow-hidden border border-gray-700 hover:border-cyan-500/50 transition-all duration-300 cursor-pointer hover:transform hover:scale-105"
        >
          <div class="h-48 bg-gradient-to-br from-cyan-500/20 to-purple-500/20 flex items-center justify-center">
            <div class="text-6xl">{{ project.icon }}</div>
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
      </div-->
      <div class="text-center text-gray-400">
        <p>Je n'ai pas encore de projets professionnels à présenter.</p>
        <p>Revenez bientôt pour découvrir mes réalisations !</p>
      </div>
      <div class="text-center mt-12">
        <a
          href="https://gabriel.blaisot.org/?lang=fr&version=cyberpunk&theme=default#projects"
          class="inline-flex items-center text-cyan-400 hover:text-cyan-300 transition-colors"
        >
          Voir mes projets personnels →
        </a>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-6 flex md:flex-row flex-col items-center gap-12 justify-center">
      <div class="aspect-square w-80 bg-gradient-to-br from-cyan-500/20 to-purple-500/20 rounded-2xl md:flex items-center justify-center border border-gray-700 hover:border-cyan-500/50 transition-all duration-300 hover:transform hover:scale-105 hidden">
        <img
          src="@/assets/icon.svg"
          alt="Avatar de Gabriel Blaisot"
          class="w-64 h-64 rounded-full object-cover shadow-lg p-2 "
        >
      </div>
      <div class="max-w-4xl flex flex-col items-start gap-4">
        <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">
          À propos de Moi
        </h2>
        <div>
          <p class="text-gray-300 mb-6 leading-relaxed">
            Développeur web freelance passionné, je me spécialise dans la création de sites web modernes et performants.
            Avec une expertise en React et Vue.js, je porte une attention particulière à l'expérience utilisateur et au design.
          </p>
          <p class="text-gray-300 mb-8 leading-relaxed">
            Disponible pour vos projets, je vous accompagne de la conception à la mise en ligne,
            en passant par le développement et l'optimisation de votre présence digitale.
          </p>
        </div>
        <div
          class="flex flex-col md:flex-row items-center gap-4 mt-6 justify-center md:justify-start w-full md:w-auto"
        >
          <a 
            href="https://gabriel.blaisot.org/?lang=fr&version=cyberpunk&theme=default#about"
            target="_blank"
            rel="noopener noreferrer"
            class="bg-gray-700 hover:bg-gray-600 text-white font-bold py-3 px-6 rounded-lg transition-colors"
          >
            Voir mon portfolio
          </a>
          <a 
            href="/CV-Gabriel-Blaisot.pdf" 
            target="_blank"
            rel="noopener noreferrer"
            class="bg-gray-700 hover:bg-gray-600 text-white font-bold py-3 px-6 rounded-lg transition-colors"
          >
            Télécharger mon CV
          </a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-6 bg-gray-800/30 flex flex-col items-center gap-12">
      <h2 class="text-4xl font-bold text-center mb-16 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent">
        Contactez-moi !
      </h2>
      <div class="max-w-4xl w-full flex-1 flex flex-col md:flex-row items-start md:items-center justify-between gap-12">
        <!-- Contact Form -->
        <div class="w-full">
          <form action="https://formspree.io/f/meogbwkq" method="POST" class="flex flex-col gap-6">
            <div>
              <label class="block text-gray-300 mb-2">Nom *</label>
              <input
                v-model="form.name"
                type="text"
                required
                name="name"
                class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:border-cyan-500 focus:outline-none transition-colors"
              >
            </div>
            <div>
              <label class="block text-gray-300 mb-2">Email *</label>
              <input
                v-model="form.email"
                type="email"
                required
                name="email"
                class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:border-cyan-500 focus:outline-none transition-colors"
              >
            </div>
            <div>
              <label class="block text-gray-300 mb-2">Type de projet</label>
              <select
                v-model="form.projectType"
                name="projectType"
                class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:border-cyan-500 focus:outline-none transition-colors"
              >
                <option value="">Sélectionnez un type</option>
                <option value="vitrine">Site Vitrine</option>
                <option value="ecommerce">E-commerce</option>
                <option value="custom">Sur mesure</option>
              </select>
            </div>
            <div>
              <label class="block text-gray-300 mb-2">Message *</label>
              <textarea
                v-model="form.message"
                required
                rows="5"
                name="message"
                class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:border-cyan-500 focus:outline-none transition-colors"
              />
            </div>
            <button
              type="submit"
              class="w-full bg-gradient-to-r from-cyan-500 to-purple-500 hover:from-cyan-600 hover:to-purple-600 text-white font-bold py-3 px-6 rounded-lg transition-all duration-300"
            >
              Envoyer le message
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="py-12 px-6 border-t border-gray-800 flex flex-col items-center">
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
      class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 flex items-center justify-center p-6"
    >
      <div
        @click.stop
        class="bg-gray-800 rounded-2xl p-8 max-w-2xl w-full border border-gray-700"
      >
        <div class="flex justify-between items-start mb-6">
          <h3 class="text-2xl font-bold text-cyan-400">{{ selectedProject.title }}</h3>
          <button @click="closeModal" class="text-gray-400 hover:text-white text-2xl">×</button>
        </div>
        <div class="h-64 bg-gradient-to-br from-cyan-500/20 to-purple-500/20 rounded-lg flex items-center justify-center mb-6">
          <div class="text-8xl">{{ selectedProject.icon }}</div>
        </div>
        <p class="text-gray-300 mb-6">{{ selectedProject.fullDescription }}</p>
        <div class="flex flex-wrap gap-2 mb-6">
          <span
            v-for="tech in selectedProject.stack"
            :key="tech"
            class="bg-gray-700 text-sm px-3 py-1 rounded-full text-gray-300"
          >
            {{ tech }}
          </span>
        </div>
        <div class="flex space-x-4">
          <button class="bg-cyan-600 hover:bg-cyan-700 text-white px-6 py-2 rounded-lg transition-colors">
            Voir le site
          </button>
          <button class="bg-gray-700 hover:bg-gray-600 text-white px-6 py-2 rounded-lg transition-colors">
            Code source
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'

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
    title: 'E-commerce Mode',
    description: 'Boutique en ligne moderne avec WooCommerce',
    fullDescription: 'Site e-commerce complet pour une marque de mode avec gestion des stocks, paiements sécurisés et interface d\'administration intuitive.',
    icon: '👗',
    stack: ['WordPress', 'WooCommerce', 'PHP', 'CSS']
  },
  {
    id: 2,
    title: 'Portfolio Architecte',
    description: 'Site vitrine élégant pour cabinet d\'architecture',
    fullDescription: 'Portfolio professionnel mettant en valeur les réalisations d\'un cabinet d\'architecture avec galerie interactive et formulaire de contact.',
    icon: '🏗️',
    stack: ['React', 'Next.js', 'Tailwind', 'Framer Motion']
  },
  {
    id: 3,
    title: 'App SaaS',
    description: 'Application web sur mesure pour gestion de projets',
    fullDescription: 'Application SaaS complète pour la gestion de projets avec authentification, dashboard temps réel et API REST.',
    icon: '📊',
    stack: ['Vue.js', 'Node.js', 'MongoDB', 'Express']
  },
  {
    id: 4,
    title: 'Restaurant Local',
    description: 'Site vitrine avec système de réservation',
    fullDescription: 'Site web pour restaurant local avec menu interactif, système de réservation en ligne et intégration Google Maps.',
    icon: '🍽️',
    stack: ['HTML', 'CSS', 'JavaScript', 'PHP']
  },
  {
    id: 5,
    title: 'Startup Tech',
    description: 'Landing page conversion-optimisée',
    fullDescription: 'Landing page haute conversion pour startup tech avec animations fluides, formulaires optimisés et tracking analytics.',
    icon: '🚀',
    stack: ['React', 'Gatsby', 'GraphQL', 'Netlify']
  },
  {
    id: 6,
    title: 'Blog Personnel',
    description: 'Blog moderne avec CMS headless',
    fullDescription: 'Blog personnel avec CMS headless, optimisation SEO avancée et performance maximale.',
    icon: '✍️',
    stack: ['Next.js', 'Strapi', 'GraphQL', 'Vercel']
  }
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
html {
  scroll-behavior: smooth;
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1f2937;
}

::-webkit-scrollbar-thumb {
  background: #06b6d4;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #0891b2;
}
</style>
