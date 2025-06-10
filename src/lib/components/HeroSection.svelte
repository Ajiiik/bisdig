<script>
  import StatCard from './StatCard.svelte';
  
  let { onSectionChange } = $props();
  
  const stats = [
    { value: '500+', label: 'Projects Done' },
    { value: '98%', label: 'Client Satisfaction' },
    { value: '5 Years', label: 'Experience' }
  ];
</script>

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
      onclick={() => onSectionChange('contact')}
      class="px-6 py-3 bg-gradient-to-r from-[#667eea] to-[#764ba2] rounded-md font-medium flex items-center gap-2 hover:opacity-90 transition-opacity"
    >
      Get Started →
    </button>
    <button
      onclick={() => onSectionChange('portfolio')}
      class="px-6 py-3 border border-gray-600 rounded-md font-medium flex items-center gap-2 hover:bg-white/5 transition-colors"
    >
      View Our Work ↗
    </button>
  </div>

  <!-- Stats -->
  <div class="flex flex-wrap gap-12 pt-8">
    {#each stats as stat}
      <StatCard value={stat.value} label={stat.label} />
    {/each}
  </div>
</div>
