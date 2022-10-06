<template>
    <div id="services">
        <div class="title-container">
            <h4>Do You Have A Construction Project We Can Help With?</h4>
        </div>
        <button class="sandwich black-btn">GET A FREE QUOTE</button>
        <div class="info-container">
            <h5 class="custom-underline">Specialists in Modern Construction</h5>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>
        </div>
        <ServicesCardComponent class="card-container"/>
        <div class="image-container">
            <!-- <img src="@/assets/img/home-244125289.jpg" alt="img"> -->
        </div>
    </div>
</template>

<script>
import ServicesCardComponent from '@/components/ServicesCardComponent.vue';
    export default {
    name: "ServicesComponent",
    components: { ServicesCardComponent }
}

</script>

<style scoped lang="scss">
    #services{
        text-align: center;

        .title-container{
            padding: 50px 30px;
            background-color: #f9d03f;
            color: #1e1e1e;
        }
        .info-container{
            padding: 80px 350px;
            h5{
                padding-bottom: 20px;
            }
            p{
                padding-top: 20px;
            }
        }
        .sandwich{
            display: block;
            position: absolute;
            left: 50%;
            transform: translateY(-50%) translateX(-50%);
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
            height: 400px;
        }
    }

</style>