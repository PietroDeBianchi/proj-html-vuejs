<script>
import AppMainService from './mainComponents/AppMainService.vue';
import AppMainFounder from './mainComponents/AppMainFounder.vue';
import AppMainEvents from './mainComponents/AppMainEvents.vue';
import AppMainBrief from './mainComponents/AppMainBrief.vue';

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
        AppMainBrief
    }
}
</script>

<template>
    <main>
        <AppMainService></AppMainService>
        <AppMainFounder></AppMainFounder>
        <AppMainEvents></AppMainEvents>
        <AppMainBrief></AppMainBrief>
    </main>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;
</style>