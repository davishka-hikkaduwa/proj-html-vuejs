<template>
    <div id="home">
        <h1>BUILDING INSPIRING SPACES</h1>
        <h6>We Build Inspiring Residential & Commercial Spaces</h6>
        <div class="row">
            <div class="col-6">
                <button class="black-btn">EXPLORE RECENT WORK</button>
            </div>
            <div class="col-6">
                <button class="yellow-btn">GET A QUOTE TODAY</button>
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
    #home{
        background-image: url("../assets/img/home-slider-62528242.jpg");
        background-repeat:no-repeat;
        background-position: fixed;
        background-size: contain;
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        h1{
            color: #fff;
        }
        h6{
            color: #f9d03f;
            margin-bottom: 26px;
        }
    }
</style>