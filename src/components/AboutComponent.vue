<template>
    <div id="about">
        <div class="core-values">
            <div class="info-container">
                <h5 class="custom-underline">Our Core Values</h5>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                    Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
                </p>
            </div>
            <AboutCardComponent class="card-container"/>
        </div>
        <div class="feedback">

        </div>
    </div>
</template>

<script>
import AboutCardComponent from "@/components/AboutCardComponent.vue";
    export default {
    name: "AboutComponent",
    components: { AboutCardComponent }
}
</script>

<style scoped lang="scss">
    #about{
        background-color: #f0ede6;
        padding: 30px 0;
        text-align: center;
        .core-values{
            .info-container{
                padding: 40px 260px 0px;
                
                p{
                    padding: 20px 40px 0px;
                }
            }
            .card-container{
                padding: 20px 200px;
                margin-bottom: 80px;
                .row{
                    flex-wrap: nowrap;
                } 
            }
        }
    }
        
</style>