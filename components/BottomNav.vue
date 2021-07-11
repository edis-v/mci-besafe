<template>
    <div class="w-full pt-24">
        <!-- <section id="bottom-navigation" class="md:hidden block fixed inset-x-0 bottom-0 z-10 bg-white shadow"> // if shown only tablet/mobile-->
        <section id="bottom-navigation" class="block fixed inset-x-0 bottom-0 z-10 bg-white shadow">
            <div id="tabs" class="flex justify-between">
                <nuxt-link
                    to="/"
                    class="w-full focus:text-blue-600 hover:text-blue-600 justify-center inline-block text-center pt-2 pb-1"
                    exact>
                    <font-awesome-icon :icon="['fas', 'home']"/>
                    <span class="tab tab-home block text-xs">Home</span>
                </nuxt-link>
                <nuxt-link
                    to="/tracker"
                    class="w-full focus:text-blue-600 hover:text-blue-600 justify-center inline-block text-center pt-2 pb-1"
                    exact>
                    <font-awesome-icon :icon="['fas', 'compass']"/>
                    <span class="tab tab-explore block text-xs">Tracker</span>
                </nuxt-link>
                <nuxt-link
                    to="/news"
                    class="w-full focus:text-blue-600 hover:text-blue-600 justify-center inline-block text-center pt-2 pb-1"
                    exact>
                    <font-awesome-icon :icon="['fas', 'rss']"/>
                    <span class="tab tab-explore block text-xs">News</span>
                </nuxt-link>
                <nuxt-link
                    to="/scannen"
                    class="w-full focus:text-blue-600 hover:text-blue-600 justify-center inline-block text-center pt-2 pb-1"
                    exact>
                    <font-awesome-icon :icon="['fas', 'qrcode']"/>
                    <span class="tab tab-account block text-xs">Scannen</span>
                </nuxt-link>
            </div>
        </section>
    </div>
</template>
