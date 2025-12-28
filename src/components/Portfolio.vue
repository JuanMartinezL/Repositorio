<template>
  <section class="portfolio" id="portfolio">
    <div class="text-center mb-6 flex flex-col gap-8">
      <h2 class="text-[40px] font-semibold text-red-500">Portfolio</h2>
      <p class="px-5 text-center leading-relaxed">
  En el transcurso de mi carrera he realizado diversos proyectos con 
  diferentes tecnologías y de distintos tipos. <br /><br />
  
  Aquí encontrarás algunos de ellos, desde los más recientes 
  hasta los más antiguos. <br /><br />
  
  Algunos son sencillos, otros más complejos, pero todos con múltiples 
  desafíos en cuanto a diseño, desarrollo e implementación, 
  los cuales me han dejado grandes lecciones.
</p>
    </div>
    <div class="flex gap-4 flex-col md:flex-row justify-center items-center mt-8 flex-wrap">
      <Card
        v-for="(portfolio, idx) in portfolios"
        :key="idx"
        :data="portfolio"
      />
    </div>
  </section>
</template>
<script>
import { defineComponent, defineAsyncComponent } from 'vue'
import portfolios from '@/assets/data/portfolio.json'

export default defineComponent({
  name: 'Portfolio',
  components: {
    Card: defineAsyncComponent(() => import('@/components/Card.vue')),
  },
  setup() {
    return {
      portfolios,
    }
  },
})
</script>
<style lang="css" scoped>
.portfolio {
  @apply p-10 md:py-20 items-center;
}
</style>
