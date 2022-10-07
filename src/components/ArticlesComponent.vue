<template>
    <div id="articles">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. 
                Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
            </p>
        </div>

    </div>
</template>

<script>
import SectionTitleComponent from './SectionTitleComponent.vue';
export default {
    name: "ArticlesComponent",
    data(){
        return {
            sectionTitle: 'Latest News',
        }
    },
    components: { 
        SectionTitleComponent 
    }
}
</script>

<style scoped lang="scss">
    #articles{
        background-color: #f0ede6;
        padding: 30px 0;
        text-align: center;
    }

</style>