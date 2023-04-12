<script>
import AppMainService from './mainComponents/AppMainService.vue';
import AppMainFounder from './mainComponents/AppMainFounder.vue';
import AppMainEvents from './mainComponents/AppMainEvents.vue';
import AppMainBrief from './mainComponents/AppMainBrief.vue';
import AppMainNews from './mainComponents/AppMainNews.vue';
import AppMainTestimonials from './mainComponents/AppMainTestimonials.vue';
import AppMainVideo from './mainComponents/AppMainVideo.vue';
import AppMainForm from './mainComponents/AppMainForm.vue';

export default {
    name: "AppMain",
    data() {
        return {
        };
    },
    components: {
        AppMainService,
        AppMainFounder,
        AppMainEvents,
        AppMainBrief,
        AppMainNews,
        AppMainTestimonials,
        AppMainVideo,
        AppMainForm
    }
}
</script>

<template>
    <main>
        <AppMainService></AppMainService>
        <AppMainFounder></AppMainFounder>
        <AppMainEvents></AppMainEvents>
        <AppMainBrief></AppMainBrief>
        <AppMainNews></AppMainNews>
        <AppMainTestimonials></AppMainTestimonials>
        <AppMainVideo></AppMainVideo>
        <AppMainForm></AppMainForm>
    </main>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;
</style>