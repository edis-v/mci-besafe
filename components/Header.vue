<template>
    <div class="z-50 sticky select-none top-0 bg-blue-700 text-white px-4 py-2 flex items-center">
        <v-btn v-if="canGoBack()" text :ripple="false" class="back-wrapper mr-4" @click="to">
            <font-awesome-icon :icon="['fas', 'arrow-left']"/>
        </v-btn>
        <span class="text-xl flex-1">
            beSafe
        </span>
        <div class="icons flex flex-row-reverse">
            <font-awesome-icon :icon="['fas', 'sync']"/>
        </div>
    </div>
</template>

<script>
module.exports = {
  methods: {
    to () {
      this.$router.go(-1)
    },
    canGoBack () {
      return this.$route.path.includes('/news/')
    }
  }
}
</script>
