<template>
    <div id="work">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                 Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
            </p>
        </div>
        <div class="row image-container">
            <div class="col-4">
                <img src="@/assets/img/project2-featured-15013609-800x800.jpg" alt="project-2-800x800">
            </div>
            <div class="col-4">
                <img src="@/assets/img/project1-featured-294276386-800x800.jpg" alt="project-1-800x800">
            </div>
            <div class="col-4">
                <img src="@/assets/img/project3-featured-189023420-800x800.jpg" alt="project-3-800x800">
            </div>
        </div>
        <div class="row link-container">
            <div class="col-4"></div>
            <div class="col-4">
                <a href="#">VIEW ALL PROJECTS</a>
            </div>
            <div class="col-4"></div>
        </div>
    </div>
</template>

<script>
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';

export default {
    name: 'WorkComponent',
    data(){
        return {
            sectionTitle: 'Explore Recent Work'
        }
    },
    components: {
    SectionTitleComponent
}
}

</script>

<style scoped lang="scss">
    #work{
        padding: 50px 0;
        text-align: center;
        
        .image-container{
            padding: 0 200px;
            .col-4{
                img{
                    max-width: 100%;
                    max-height: 100%;
                }
            }
        }
        .link-container{
            padding: 60px 200px;
            .col-4{
                a{
                    text-decoration: none;
                    font-size: 0.8rem;
                }
            }
            .col-4:first-child{
                border-top: 1px solid #f0ede6;
            }
            .col-4:last-child{
                border-bottom: 1px solid #f0ede6;
            }
            
        }
    }
</style>