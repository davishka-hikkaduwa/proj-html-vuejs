<template>
    <div id="about">
        <div class="core-values">
            <div class="info-container">
                <h5 class="custom-underline">Our Core Values</h5>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                    Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
                </p>
            </div>
            <div class="card-container">
                
            </div>
        </div>
        <div class="feedback">

        </div>
    </div>
</template>

<script>
    export default {
        name: 'AboutComponent',
    }
</script>

<style scoped lang="scss">
    #about{
        background-color: #f0ede6;
        padding: 30px 0;
        text-align: center;
        .core-values{
            .info-container{
                padding: 80px 260px 20px 260px;
                h5{
                    padding-bottom: 20px;
                }
                p{
                    padding: 20px 40px;
                }
            }
        }
    }
        
</style>