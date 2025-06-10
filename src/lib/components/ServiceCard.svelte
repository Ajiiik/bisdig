<script>
  let { icon, title, description, className = '' } = $props();

  const SvelteComponent = $derived(icon);
</script>

<div class="bg-[#1E293B]/50 backdrop-blur-sm p-6 rounded-lg border border-gray-800 {className}">
  <div class="w-12 h-12 bg-[#667eea]/20 rounded-lg flex items-center justify-center mb-4">
    <SvelteComponent class="w-6 h-6 text-[#667eea]" />
  </div>
  <h3 class="text-xl font-semibold mb-2">{title}</h3>
  <p class="text-gray-400 text-sm">{description}</p>
</div>
