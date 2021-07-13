<template>
  <div class="p-6 container mx-auto md:px-24" style="max-width: 900px">
      <h1 class="mb-4">News</h1>
      <div class="shadow-lg p-4 mb-4">
          <h2>Bye Corona! Alles wird aufgemacht</h2>
          <div class="text-gray-700 text-sm">Erschienen am 01.01.2021</div>
          <div class="text-gray-700 text-sm mb-4">Autor: Max Mustermann</div>
          <p class="mb-6">
              In NRW treten am Freitag (09.07.2021) neue Corona-Regeln in Kraft. Für Kreise und Städte mit besonders niedrigem Infektionsgeschehen gilt dann mit weiteren Lockerungen die Inzidenzstufe 0.
          </p>
          <nuxt-link to="/news/bye-corona" exact class="mt-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">ZEIG MIR MEHR</nuxt-link>
      </div>

      <div class="shadow-lg p-4">
          <h2>Lockerungen in der Gastronomie</h2>
          <div class="text-gray-700 text-sm">Erschienen am 01.01.2021</div>
          <div class="text-gray-700 text-sm mb-4">Autor: Max Mustermann</div>
          <p class="mb-6">
              Die NRW-Landesregierung hat angesichts sinkender Corona-Zahlen weitere Öffnungsschritte bekanntgegeben.
          </p>
          <nuxt-link to="/news/lockerungen-gastro" exact class="mt-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">ZEIG MIR MEHR</nuxt-link>
      </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>
