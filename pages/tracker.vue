<template>
<div>
  <div class="flex w-full">
    <a href="#" class="flex-1 bg-blue-500 text-center py-2 text-white hover:bg-blue-600">
      <font-awesome-icon :icon="['fas', 'info']"/>
      Info
    </a>
    <a href="#" class="flex-1 bg-blue-500 text-center py-2 text-white hover:bg-blue-600">
      <font-awesome-icon :icon="['fas', 'map']"/>
      Kontakte
    </a>
  </div>
  <div class="p-6 container mx-auto md:px-24" style="max-width: 900px">
      <h1 class="mb-4">Eigenes Infektionsrisiko</h1>
        <div class="border-solid border-2 border-red-400 rounded-md px-4 py-4 inline-block mb-8">
          <h2 class="text-red-400 font-bold mb-2">Potentiell infiziert</h2>
          <p class="text-xs sm:text-sm mb-4">Sie waren, soweit wir das sagen können, in den letzten 14 Tagen in Kontakt mit jemanden, der potentiell infiziert ist</p>
          <a href="#" class="bg-red-400 text-white px-4 py-2 text-center w-full text-xs sm:text-sm">INFEKTION MELDEN</a>
        </div>
        <div class="shadow-md mb-8">
            <div class="tab w-full overflow-hidden border-t">
               <input class="absolute opacity-0" id="tab-single-one" type="radio" name="tabs2">
               <label class="block p-5 leading-normal cursor-pointer text-red-500" for="tab-single-one">Diese Woche</label>
               <div class="tab-content overflow-hidden border-l-2 border-red-500 leading-normal">
                  <div class="tab w-full overflow-hidden border-t">
                    <label class="block p-5 leading-normal cursor-pointer text-red-500" for="tab-single-one">Heute - Dienstag</label>
                  </div>
                  <div class="tab w-full overflow-hidden border-t">
                    <label class="block p-5 leading-normal cursor-pointer text-red-500" for="tab-single-one">Gestern - Montag</label>
                  </div>
                  <div class="leading-normal">
                        <div class="p-5">
                          <ul class="border-solid border-2 border-red-400 rounded-md px-4 py-4 mb-8">
                            <li><font-awesome-icon class="text-red-500 mr-2" :icon="['fas', 'user']"/> ID: beSafe Benutzer ****</li>
                            <li><font-awesome-icon class="text-red-500 mr-2" :icon="['fas', 'clock']"/> 17:30</li>
                            <li><font-awesome-icon class="text-red-500 mr-2" :icon="['fas', 'map-marker-alt']"/> Köln, Innenstadt, Schildergasse</li>
                          </ul>
                          <a href="#" class="mt-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm mb-4">Auf Karte anzeigen</a>
                        </div>
                  </div>
               </div>
            </div>
      </div>
  </div>
</div>
</template>

<script>
export default {}
</script>

<style lang="postcss" scoped>
         /* Tab content - closed */
         .tab-content {
         max-height: 0;
         -webkit-transition: max-height .35s;
         -o-transition: max-height .35s;
         transition: max-height .35s;
         }
         /* :checked - resize to full height */
         .tab input:checked ~ .tab-content {
         max-height: 100vh;
         }
         /* Label formatting when open */
         .tab input:checked + label{
         @apply text-xl p-5 border-l-2 border-red-500;
         font-size: 1.25rem; /*.text-xl*/
         padding: 1.25rem; /*.p-5*/
         border-left-width: 2px; /*.border-l-2*/
         }
         /* Icon */
         .tab label::after {
         float:right;
         right: 0;
         top: 0;
         display: block;
         width: 1.5em;
         height: 1.5em;
         line-height: 1.5;
         font-size: 1.25rem;
         text-align: center;
         -webkit-transition: all .35s;
         -o-transition: all .35s;
         transition: all .35s;
         }
         /* Icon formatting - closed */
         .tab input[type=checkbox] + label::after {
         content: "+";
         font-weight:bold; /*.font-bold*/
         border-width: 1px; /*.border*/
         border-radius: 9999px; /*.rounded-full */
         border-color: #b8c2cc; /*.border-grey*/
         }
         .tab input[type=radio] + label::after {
         content: "\25BE";
         font-weight:bold; /*.font-bold*/
         border-width: 1px; /*.border*/
         border-radius: 9999px; /*.rounded-full */
         border-color: #b8c2cc; /*.border-grey*/
         }
         /* Icon formatting - open */
         .tab input[type=checkbox]:checked + label::after {
         transform: rotate(315deg);
         background-color: red; /*.bg-indigo*/
         color: #f8fafc; /*.text-grey-lightest*/
         }
         .tab input[type=radio]:checked + label::after {
         transform: rotateX(180deg);
         color: red; /*.text-grey-lightest*/
         }
</style>
