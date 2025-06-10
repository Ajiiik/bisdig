<script>
  let { activeSection, onSectionChange } = $props();
  
  const navItems = [
    { id: 'services', label: 'Services', emoji: '⚙️' },
    { id: 'portfolio', label: 'Portfolio', emoji: '🖼️' },
    { id: 'about', label: 'About', emoji: '👤' },
    { id: 'contact', label: 'Contact', emoji: null }
  ];
</script>

<header class="container mx-auto px-4 py-6">
  <nav class="flex justify-between items-center">
    <button 
      onclick={() => onSectionChange('home')} 
      class="text-[#667eea] text-xl font-bold hover:opacity-80 transition-opacity"
    >
      WebCraft Ali
    </button>
    <div class="flex items-center gap-8">
      {#each navItems as item}
        <button 
          onclick={() => onSectionChange(item.id)} 
          class="flex items-center gap-2 text-gray-300 hover:text-white transition-colors"
          class:text-white={activeSection === item.id}
        >
          {#if item.emoji}
            <span class="w-5 h-5 rounded-full border border-gray-500 flex items-center justify-center text-xs">
              {item.emoji}
            </span>
          {/if}
          {item.label}
        </button>
      {/each}
    </div>
  </nav>
</header>
