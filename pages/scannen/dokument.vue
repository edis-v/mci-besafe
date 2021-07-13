<template>
  <div v-if="state == 'none'" class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <div>
        <h1 class="mb-4">Ein Dokument hinzufügen</h1>
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
        <h1 class="mb-4">Ein Dokument hinzufügen</h1>
        <div class="m-auto">
            <div>
                <div class="bg-gray-200 m-auto flex justify-center p-4">
                <img src="~/assets/qr.png" />
            </div>
            <div class="leading-normal">
                        <div class="p-5">
                          <ul class="border-solid border-2 border-gray-200 rounded-md px-4 py-4 mb-8">
                              <li class="mb-2">Aktueller PCR-Test</li>
                            <li class="mb-4"><font-awesome-icon class="text-green-500 mr-2" :icon="['fas', 'clock']"/>01.01.2021</li>
                            <a @click="state = 'confirmed'" href="#" class="my-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">Jetzt hinzufügen</a>
                          </ul>
                        </div>
                  </div>
            </div>
        </div>
    </div>
  </div>
  <div v-else class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <div class="flex items-center">
        <div class="m-auto flex-row align-center items-center">
            <p class="mb-4">
                <font-awesome-icon class="text-green-500 mr-2 text-xl text-center" :icon="['fas', 'check-circle']"/> Ihr aktueller PCR-Test vom 01.01.2021 wurde erfolgreich registriert.
            </p>
            <nuxt-link to="/scannen" class="my-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">Zurück</nuxt-link>
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
