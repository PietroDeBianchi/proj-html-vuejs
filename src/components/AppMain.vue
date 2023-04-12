<script>
import AppMainService from './mainComponents/AppMainService.vue';
import AppMainFounder from './mainComponents/AppMainFounder.vue';
import AppMainEvents from './mainComponents/AppMainEvents.vue';

export default {
    name: "AppMain",
    data() {
        return {
        };
    },
    components: {
        AppMainService,
        AppMainFounder,
        AppMainEvents
    }
}
</script>

<template>
    <AppMainService></AppMainService>
    <AppMainFounder></AppMainFounder>
    <AppMainEvents></AppMainEvents>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;
</style>