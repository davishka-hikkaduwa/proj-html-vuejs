<template>
    <div id="home">
        <h1>BUILDING INSPIRING SPACES</h1>
        <h6>We Build Inspiring Residential & Commercial Spaces</h6>
        <div class="row">
            <div class="col-6">
                <button class="black-btn">EXPLORE RECENT WORK</button>
            </div>
            <div class="col-6">
                <button class="gold-btn">GET A QUOTE TODAY</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HomeComponent',
    }
</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

    #home{
        background-image: url("../assets/img/home-slider-62528242.jpg");
        background-repeat:no-repeat;
        background-size: cover;
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        h1{
            color: $white-color;
        }
        h6{
            color: $bright-sun-color;
            margin-bottom: 26px;
        }
    }
</style>