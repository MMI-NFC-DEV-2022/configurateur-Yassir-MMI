<template>
  <header class="bg-pink-500 text-white body-font shadow w-full">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <nav class="flex lg:w-2/5 flex-wrap items-center text-base md:ml-auto">
        <RouterLink to="/" class="mr-5 hover:text-gray-900 cursor-pointer">Accueil</RouterLink>
        <RouterLink to="/formulaire1" class="mr-5 hover:text-gray-900 cursor-pointer">Formulaire1</RouterLink>
        <RouterLink to="/formulaire2" class="mr-5 hover:text-gray-900 cursor-pointer">Formulaire2</RouterLink>
        
        
      </nav>
      <a class="flex order-first lg:order-none lg:w-1/5 title-font font-medium items-center text-gray-900 lg:items-center lg:justify-center mb-4 md:mb-0">
        <span class="text-xl">Le site de bral zinc</span>
      </a>
      <div class="lg:w-2/5 inline-flex lg:justify-end ml-5 lg:ml-0">
        <button class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0 text-pink-500">Se connecter
          <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
/* Aucun style supplémentaire nécessaire ici si vous utilisez Tailwind */
</style>
