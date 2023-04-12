<script>
import AppMainService from './mainComponents/AppMainService.vue';
import AppMainFounder from './mainComponents/AppMainFounder.vue';

export default {
    name: "AppMain",
    data() {
        return {
        };
    },
    components: {
        AppMainService,
        AppMainFounder
    }
}
</script>

<template>
    <AppMainService></AppMainService>
    <AppMainFounder></AppMainFounder>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;
</style>