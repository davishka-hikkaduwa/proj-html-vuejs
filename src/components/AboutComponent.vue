<template>
    <div id="about">
        <div class="core-values">
            <div class="info-container">
                <SectionTitleComponent :title="coreValuesSectionTitle"/>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>
            </div>
            <AboutCardComponent class="card-container"/>
        </div>
        <div class="feedback">
            <div class="top-curved-space"></div>
            <div class="info-container">
                <SectionTitleComponent :title="feedbackSectionTitle"/>
                <img src="@/assets/img/home-testimonial-113165296.jpg" alt="home-testimonial">
                <p>"Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                    Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi."
                </p>
                <h6>HARRY SMITH - NEW HOME OWNER</h6>
            </div>
            <div class="bottom-curved-space"></div>
        </div>
    </div>
</template>

<script>

import AboutCardComponent from "@/components/AboutCardComponent.vue";
import SectionTitleComponent from "@/components/SectionTitleComponent.vue";
    export default {
    name: "AboutComponent",
    data(){
        return {
            coreValuesSectionTitle: 'Our Core Values',
            feedbackSectionTitle: 'Our Home Owners Say'
        }
    },
    components: {
        AboutCardComponent, 
        SectionTitleComponent
    }
}
</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

    #about{
        background-color: $pampas-color;
        padding: 30px 0;
        text-align: center;

        .core-values{
            .card-container{
                padding: 20px 200px;
                margin-bottom: 80px;
                .row{
                    flex-wrap: nowrap;
                } 
            }     
        }
        .feedback{
            padding-top: 80px;
            padding-bottom: 80px;
            color: $white-color;
            background-image: url('@/assets/img/home-parallax-144609983.jpg');
            background-repeat:no-repeat;
            background-size: cover;
            position: relative;
            height: 700px;

            .top-curved-space,
            .bottom-curved-space {
                background-color: $pampas-color;
            }
            
            .info-container{
                img{
                    margin-top: 20px;
                    border-radius: 50%;
                }
                h6{
                    padding-top: 10px;
                }
            }
        }
    }
        
</style>