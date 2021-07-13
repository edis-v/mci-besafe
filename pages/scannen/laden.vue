<template>
  <div v-if="state == 'none'" class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <div>
        <h1 class="mb-4">Einen Laden besuchen</h1>
        <div class="m-auto">
            <div>
                <div class="bg-gray-200 m-auto flex justify-center p-4">
                <img src="~/assets/qr.png" />
            </div>
            <div @click="state = 'scanned'" class="m-auto mt-4 rounded-full h-24 w-24 flex items-center justify-center bg-red-600 border-8 border-gray-200"></div>
            </div>
        </div>
    </div>
  </div>
  <div v-else-if="state == 'scanned'" class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <div>
        <h1 class="mb-4">Gescannter Code</h1>
        <div class="m-auto">
            <div>
                <div class="bg-gray-200 m-auto flex justify-center p-4">
                <img src="~/assets/qr.png" />
            </div>
            <div class="leading-normal">
                        <div class="p-5">
                          <ul class="border-solid border-2 border-gray-200 rounded-md px-4 py-4 mb-8">
                            <li><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'clock']"/>17:30</li>
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'map-marker-alt']"/>REWE Frischemarkt, Köln</li>
                            <a @click="state = 'confirmed'" href="#" class="my-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">Jetzt einbuchen</a>
                            <!--<nuxt-link to="/scannen" class="my-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">Jetzt einbuchen</nuxt-link>-->
                          </ul>
                        </div>
                  </div>
            </div>
        </div>
    </div>
  </div>
  <div v-else class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <div>
        <h1 class="mb-4">Erfolgreich eingebucht</h1>
                        <div class="mx-2">
                          <ul class="border-solid border-2 border-green-500 rounded-md px-4 py-4 mb-6">
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'map-marker-alt']"/>REWE Frischemarkt, Köln</li>
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'users']"/>Aktuelle Besucher: 14</li>
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'check']"/>Kein PCR-Test nötig</li>
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'check']"/>Kein Schnelltest nötig</li>
                            <li><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'check']"/>Maximale Besucher 100</li>
                          </ul>
                        </div>
                        <div class="mx-2">
                          <div class="border-solid border-2 border-green-500 rounded-md px-4 py-4 mb-8">
                              <div class="mb-4">Sorgenlos einkaufen</div>
                              <p class="my-4">Sie können den ‘Rewe Frischemarkt’ gerne betretene. Aktuell benöttigen sie keinen negativen Test.</p>
                            <nuxt-link to="/scannen" class="my-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">Verstanden</nuxt-link>
                          </div>
                        </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      state: 'none' // none, scanned, confirmed
    }
  }
}
</script>

<style>
</style>
