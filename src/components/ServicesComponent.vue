<template>
    <div id="services">
        <div class="heading-container">
            <h4>Do You Have A Construction Project We Can Help With?</h4>
        </div>
        <div class="info-container">
            <h5>Specialists in Modern Construction</h5>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>
        </div>
        <div class="card-container">
            
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ServicesComponent',
    }

</script>

<style scoped lang="scss">
    #services{
        text-align: center;

        .heading-container{
            padding: 30px 30px;
            background-color: #f9d03f;
            color: #1e1e1e;
        }
        .info-container{
            padding: 80px 200px;
            h5{
                padding-bottom: 20px;
                position: relative;
            }
            h5::before{
                content: '';
                position: absolute;
                bottom: 0;
                left: 40%;
                width: 140px;
                height: 2px;
                background-color: #f9d03f;
            }
            p{
                padding-top: 20px;
            }
        }
    }

</style>