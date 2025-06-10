<script>
  import { Palette, Zap, Rocket } from 'lucide-svelte';
  
  let activeSection = $state('home');
  
  function scrollToSection(sectionId) {
    activeSection = sectionId;
    // In a real app, you'd implement smooth scrolling here
  }
</script>

<div class="min-h-screen bg-gradient-to-br from-[#1a1a2e] to-[#16213e] text-white overflow-hidden relative">
  <!-- Background decorative elements -->
  <div class="absolute top-[90px] right-[90px] w-[300px] h-[300px] rounded-full bg-[#667eea]/10 blur-3xl"></div>
  <div class="absolute bottom-[90px] left-[90px] w-[300px] h-[300px] rounded-full bg-[#667eea]/10 blur-3xl"></div>

  <!-- Navigation -->
  <header class="container mx-auto px-4 py-6">
    <nav class="flex justify-between items-center">
      <button onclick={() => scrollToSection('home')} class="text-[#667eea] text-xl font-bold hover:opacity-80 transition-opacity">
        WebCraft Ali
      </button>
      <div class="flex items-center gap-8">
        <button onclick={() => scrollToSection('services')} class="flex items-center gap-2 text-gray-300 hover:text-white transition-colors">
          <span class="w-5 h-5 rounded-full border border-gray-500 flex items-center justify-center text-xs">
            ⚙️
          </span>
          Services
        </button>
        <button onclick={() => scrollToSection('portfolio')} class="flex items-center gap-2 text-gray-300 hover:text-white transition-colors">
          <span class="w-5 h-5 rounded-full border border-gray-500 flex items-center justify-center text-xs">
            🖼️
          </span>
          Portfolio
        </button>
        <button onclick={() => scrollToSection('about')} class="flex items-center gap-2 text-gray-300 hover:text-white transition-colors">
          <span class="w-5 h-5 rounded-full border border-gray-500 flex items-center justify-center text-xs">
            👤
          </span>
          About
        </button>
        <button onclick={() => scrollToSection('contact')} class="text-gray-300 hover:text-white transition-colors">
          Contact
        </button>
      </div>
    </nav>
  </header>

  <!-- Main Content -->
  <main class="container mx-auto px-4 py-16">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <!-- Left Column - Hero Content -->
      <div class="space-y-8">
        <h1 class="text-5xl font-bold leading-tight">
          <span class="text-white">Crafting </span>
          <span class="bg-gradient-to-r from-[#667eea] to-[#764ba2] bg-clip-text text-transparent">
            Digital Experiences{" "}
          </span>
          <span class="text-[#667eea]">That Convert</span>
        </h1>

        <p class="text-gray-300 text-lg max-w-xl">
          We design and develop stunning websites that not only look amazing but drive real business results. From
          concept to launch, we're your digital partners.
        </p>

        <div class="flex flex-wrap gap-4">
          <button
            onclick={() => scrollToSection('contact')}
            class="px-6 py-3 bg-gradient-to-r from-[#667eea] to-[#764ba2] rounded-md font-medium flex items-center gap-2 hover:opacity-90 transition-opacity"
          >
            Get Started →
          </button>
          <button
            onclick={() => scrollToSection('portfolio')}
            class="px-6 py-3 border border-gray-600 rounded-md font-medium flex items-center gap-2 hover:bg-white/5 transition-colors"
          >
            View Our Work ↗
          </button>
        </div>

        <!-- Stats -->
        <div class="flex flex-wrap gap-12 pt-8">
          <div class="text-center">
            <div class="text-[#667eea] text-3xl font-bold">500+</div>
            <div class="text-gray-400 text-sm">Projects Done</div>
          </div>
          <div class="text-center">
            <div class="text-[#667eea] text-3xl font-bold">98%</div>
            <div class="text-gray-400 text-sm">Client Satisfaction</div>
          </div>
          <div class="text-center">
            <div class="text-[#667eea] text-3xl font-bold">5 Years</div>
            <div class="text-gray-400 text-sm">Experience</div>
          </div>
        </div>
      </div>

      <!-- Right Column - Service Cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-[#1E293B]/50 backdrop-blur-sm p-6 rounded-lg border border-gray-800">
          <div class="w-12 h-12 bg-[#667eea]/20 rounded-lg flex items-center justify-center mb-4">
            <Palette class="w-6 h-6 text-[#667eea]" />
          </div>
          <h3 class="text-xl font-semibold mb-2">UI/UX Design</h3>
          <p class="text-gray-400 text-sm">Beautiful, intuitive interfaces that users love to interact with.</p>
        </div>

        <div class="bg-[#1E293B]/50 backdrop-blur-sm p-6 rounded-lg border border-gray-800">
          <div class="w-12 h-12 bg-[#667eea]/20 rounded-lg flex items-center justify-center mb-4">
            <Zap class="w-6 h-6 text-[#667eea]" />
          </div>
          <h3 class="text-xl font-semibold mb-2">Fast Development</h3>
          <p class="text-gray-400 text-sm">Lightning-fast websites optimized for performance and SEO.</p>
        </div>

        <div class="md:col-span-2 bg-[#1E293B]/50 backdrop-blur-sm p-6 rounded-lg border border-gray-800">
          <div class="w-12 h-12 bg-[#667eea]/20 rounded-lg flex items-center justify-center mb-4">
            <Rocket class="w-6 h-6 text-[#667eea]" />
          </div>
          <h3 class="text-xl font-semibold mb-2">Full-Stack Solutions</h3>
          <p class="text-gray-400 text-sm">
            Complete web solutions from frontend design to backend development, deployment, and ongoing maintenance.
          </p>
        </div>
      </div>
    </div>
  </main>
</div>

<style>
  :global(body) {
    margin: 0;
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  }
  
  :global(*) {
    box-sizing: border-box;
  }
</style>
