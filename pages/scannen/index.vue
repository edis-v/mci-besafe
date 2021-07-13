<template>
  <div class="p-6 container mx-auto md:px-24" style="max-width: 900px">
    <h1 class="mb-4">Barcode scannen</h1>
    <div class="shadow-lg p-4 mb-4">
          <h2 class="mb-4">Einen Laden besuchen</h2>
          <p class="mb-6">
            Wählen Sie diese Funktion, wenn Sie einen Laden besuchen und den zugehörigen QR-Code scannen möchten.
          </p>
          <nuxt-link to="/scannen/laden" class="bg-blue-600 text-white px-4 py-2 text-center w-full text-xs sm:text-sm uppercase">Jetzt Scannen</nuxt-link>
      </div>
    <div class="shadow-lg p-4 mb-4">
          <h2 class="mb-4">Dokument hinzufügen</h2>
          <p class="mb-6">
            Wählen Sie diese Funktion, wenn Sie ein neues Corona Dokument hinterlegen und den zugehörigen QR-Code scannen möchten.
          </p>
          <nuxt-link to="/scannen/dokument" class="bg-blue-600 text-white px-4 py-2 text-center w-full text-xs sm:text-sm uppercase">Jetzt Scannen</nuxt-link>
      </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
</style>
