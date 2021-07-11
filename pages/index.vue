<template>
  <div>
    <div class="bg-cover bg-center bg-scroll h-32 sm:h-48 w-full flex items-center justify-center" style="background-image: url(https://www.eon.de/content/dam/eon/eon-de-zwei/images/landschaft/koeln/koeln_111x80.jpg/jcr:content/renditions/cq5dam.web.800.1000.jpeg)">
      <div class="font-bold py-6 h-24 w-24 sm:h-32 sm:w-32 opacity-90 text-gray-700 rounded-full bg-white border-solid border-4 border-green-400 flex items-center justify-center">
        <div class="flex font-sans text-xs sm:text-sm flex-col items-center">
          <p>Köln</p>
          <p>493 Infizierte</p>
          <p>IZW: 12,5</p>
        </div>
      </div>
    </div>
    <div class="p-6 container mx-auto md:px-24" style="max-width: 900px">
      <h1 class="mb-4">Eigenes Infektionsrisiko</h1>
      <div class="border-solid border-2 border-green-400 rounded-md px-4 py-4 inline-block">
        <h2 class="text-green-400 font-bold mb-2">Alles in Ordnung</h2>
        <p class="text-xs sm:text-sm mb-4">Sie waren, soweit wir das sagen können, in den letzten 14 Tagen nicht in Kontakt mit jemanden, der potentiell infiziert ist.</p>
        <nuxt-link to="/tracker" class="bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">ZUM TRACKER</nuxt-link>
      </div>
      <h1 class="mb-4 mt-8">Infos für mich</h1>
      <div class="shadow-md mb-8">
            <div class="tab w-full overflow-hidden border-t">
               <input class="absolute opacity-0" id="tab-single-one" type="radio" name="tabs2">
               <label class="block p-5 leading-normal cursor-pointer" for="tab-single-one">Allgemein</label>
               <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">
                  <p class="p-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.</p>
               </div>
            </div>
            <div class="tab w-full overflow-hidden border-t">
               <input class="absolute opacity-0" id="tab-single-two" type="radio" name="tabs2">
               <label class="block p-5 leading-normal cursor-pointer" for="tab-single-two">Elternteil</label>
               <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">
                  <p class="p-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.</p>
               </div>
            </div>
            <div class="tab w-full overflow-hidden border-t">
               <input class="absolute opacity-0" id="tab-single-three" type="radio" name="tabs2">
               <label class="block p-5 leading-normal cursor-pointer" for="tab-single-three">Nutzung von öffentlichen Verkehrsmitteln</label>
               <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">
                  <p class="p-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.</p>
               </div>
            </div>
      </div>
      <nuxt-link to="/news" class="mt-4 bg-gray-300 px-4 py-2 text-center w-full text-xs sm:text-sm">ZU DEN NEWS</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>

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
         /*@apply text-xl p-5 border-l-2 border-indigo-500 bg-gray-100 text-indigo*/
         font-size: 1.25rem; /*.text-xl*/
         padding: 1.25rem; /*.p-5*/
         border-left-width: 2px; /*.border-l-2*/
         border-color: #6574cd; /*.border-indigo*/
         background-color: #f8fafc; /*.bg-gray-100 */
         color: #6574cd; /*.text-indigo*/
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
         background-color: #6574cd; /*.bg-indigo*/
         color: #f8fafc; /*.text-grey-lightest*/
         }
         .tab input[type=radio]:checked + label::after {
         transform: rotateX(180deg);
         background-color: #6574cd; /*.bg-indigo*/
         color: #f8fafc; /*.text-grey-lightest*/
         }
</style>
