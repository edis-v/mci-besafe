<template>
    <div v-if="state != 'done'" class="absolute w-screen h-screen bg-gray-50 z-50 flex content-center">
        <div class="m-w-64 m-auto">
            <h1 class="text-center text-blue-600 text-2xl mb-2">beSafe</h1>
            <div v-if="state == 'info'" class="inset-x-0 bg-gray-250 shadow text-sm p-4" style="max-width: 70ch;">
                <p class="mb-4">Damit Sie auch alle für Sich relevanten Infos erhalten, benötigen wir zunächst Ihre Hilfe.</p>
                <p class="mb-4">Füllen Sie bitte dafür den von uns vorbereiteten Fraebogen aus.</p>
                <p class="mb-4">Dafür ist weder eine Registrierung nötig, noch übermitteln wir Ihr Formular an einen Server.</p>
                <p>Alles bleibt sicher auf Ihrem Gerät gespeichert.</p>
                <button @click="showWizard" class="bg-blue-500 mt-4 text-white px-4 py-2 text-center w-full text-xs sm:text-sm">ZUM FRAGEBOGEN</button>
            </div>
            <div v-else class="inset-x-0 bg-gray-250 shadow text-sm p-4" style="max-width: 70ch;">
                <p class="mb-4">Damit Sie auch alle für Sich relevanten Infos erhalten brauchen wir zunächst Ihre Hilfe.</p>
                <p class="mb-4">Füllen Sie dazu den von uns vorbereiteten Fraebogen aus.</p>
                <form class="w-full max-w-lg">
                    <div>
                        <h2 class="mb-4 font-bold tracking-wide uppercase text-xs">Allgemeine Daten</h2>
                        <div class="w-full">
                        <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-age">
                            Alter
                        </label>
                        <input class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white" id="grid-age" type="number">
                        </div>
                        <div class="w-full">
                            <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-job">
                                Aktuelle Beschäftigung
                            </label>
                            <div class="relative">
                                <select class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500" id="grid-job">
                                    <option>Schüler/Student</option>
                                    <option>Berufstätig</option>
                                    <option>Unternehmer</option>
                                    <option>ohne Arbeit</option>
                                </select>
                                <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                                <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/></svg>
                                </div>
                            </div>
                        </div>
                        <div class="w-full my-4 mb-6">
                            <input class="mr-2 leading-tight" type="checkbox">
                            <span class="text-sm">
                                Nutze öffentliche Verkehrsmittel
                            </span>
                        </div>
                    </div>
                    <h2 class="my-4 font-bold tracking-wide uppercase text-xs">Freizeitaktivitäten</h2>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-4 py-2 text-xs rounded-full text-blue-600 border border-blue-600 undefined">Shopping</span>
                        <span class="px-4 py-2 text-xs rounded-full text-blue-600 border border-blue-600 undefined">Gemeinschaftssport</span>
                        <span class="px-4 py-2 text-xs rounded-full text-blue-600 border border-blue-600 undefined">Freunde treffen</span>
                        <span class="px-4 py-2 text-xs rounded-full text-blue-600 border border-blue-600 undefined">+</span>
                    </div>
                </form>
                <button @click="saveAndContinue" class="bg-blue-500 mt-6 text-white px-4 py-2 text-center w-full text-xs sm:text-sm uppercase">Speichern und Weiter</button>
            </div>
        </div>
    </div>
</template>

<script>
module.exports = {
  data () {
    return {
      state: 'info' // info, wizard, done
    }
  },
  methods: {
    showWizard () {
      this.state = 'wizard'
    },
    saveAndContinue () {
      this.state = 'done'
    }
  }
}
</script>
