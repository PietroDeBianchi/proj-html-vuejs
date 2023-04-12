<script>
import AppMainService from './mainComponents/AppMainService.vue';

export default {
    name: "AppMain",
    data() {
        return {
        };
    },
    components: {
        AppMainService,
    }
}
</script>

<template>
    <AppMainService></AppMainService>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins";
@use "../styles/partials/variables" as *;
</style>