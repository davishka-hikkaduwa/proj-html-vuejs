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
            <div class="info-container">
                <h5 class="custom-underline">Our Home Owners Say</h5>
                <img src="@/assets/img/home-testimonial-113165296.jpg" alt="home-testimonial">
                <p>"Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                    Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi."
                </p>
                <h6>HARRY SMITH - NEW HOME OWNER</h6>
            </div>
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

        .info-container{
            padding: 40px 260px 0px;
                
            p{
                padding: 20px 40px 0px;
            }
        }

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
            color: #fff;
            background-image: url('@/assets/img/home-parallax-144609983.jpg');
            background-repeat:no-repeat;
            background-size: cover;
            
            .info-container{
                img{
                    margin-top: 20px;
                    border-radius: 50%;
                }
                h6{
                    padding-top: 20px;
                }
            }
        }
    }
        
</style>