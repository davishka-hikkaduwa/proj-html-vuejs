<template>
    <main>
        <HomeComponent/>
        <ServicesComponent/>
        <WorkComponent/>
    </main>
</template>

<script>
import HomeComponent from '@/components/HomeComponent.vue';
import ServicesComponent from '@/components/ServicesComponent.vue';
import WorkComponent from '@/components/WorkComponent.vue';
export default {
    name: "MainComponent",
    components: {
    HomeComponent,
    ServicesComponent,
    WorkComponent
}
}
</script>

<style scoped lang="scss">

</style>