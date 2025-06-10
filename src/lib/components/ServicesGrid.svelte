<script>
  import { Palette, Zap, Rocket } from 'lucide-svelte';
  import ServiceCard from './ServiceCard.svelte';
  
  const services = [
    {
      icon: Palette,
      title: 'UI/UX Design',
      description: 'Beautiful, intuitive interfaces that users love to interact with.'
    },
    {
      icon: Zap,
      title: 'Fast Development',
      description: 'Lightning-fast websites optimized for performance and SEO.'
    },
    {
      icon: Rocket,
      title: 'Full-Stack Solutions',
      description: 'Complete web solutions from frontend design to backend development, deployment, and ongoing maintenance.',
      className: 'md:col-span-2'
    }
  ];
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
  {#each services as service}
    <ServiceCard 
      icon={service.icon}
      title={service.title}
      description={service.description}
      className={service.className || ''}
    />
  {/each}
</div>
