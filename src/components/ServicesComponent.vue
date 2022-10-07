<template>
    <div id="services">
        <div class="label-container">
            <h4>Do You Have A Construction Project We Can Help With?</h4>
        </div>
        <button class="sandwich-btn black-btn">GET A FREE QUOTE</button>
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>
        </div>
        <ServicesCardComponent class="card-container"/>
        <div class="image-container">
            <div class="top-curved-space"></div>
            <div class="bottom-curved-space"></div>
        </div>
    </div>
</template>

<script>
import ServicesCardComponent from '@/components/ServicesCardComponent.vue';
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';
    export default {
    name: "ServicesComponent",
    data(){
        return {
            sectionTitle: 'Specialists in Modern Construction'
        }
    },
    components: {
    ServicesCardComponent,
    SectionTitleComponent
},
}

</script>

<style scoped lang="scss">
    #services{
        text-align: center;

        .label-container{
            padding: 50px 30px;
            background-color: #f9d03f;
            color: #1e1e1e;
        }
 
        .sandwich-btn{
            display: block;
            position: absolute;
            border: 2px solid #fff;
            left: 50%;
            transform: translateY(-50%) translateX(-50%);
        }
        .sandwich-btn:hover{
            background-color: #fff;
            color: #1e1e1e;
            border: 2px solid #1e1e1e;
        }
        .card-container{
            padding: 20px 60px;
            margin-bottom: 80px;
            .row{
                flex-wrap: nowrap;
            }    
        }
        
        .image-container{
            background-image: url('@/assets/img/home-244125289.jpg');
            background-repeat:no-repeat;
            background-size: cover;
            height: 600px;
            position: relative;

            .top-curved-space,
            .bottom-curved-space {
                background-color: #fff;
            }
        }
    }

</style>