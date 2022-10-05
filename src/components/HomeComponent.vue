<template>
    <div id="home">
        <h1>BUILDING INSPIRING SPACES</h1>
        <h4>We Build Inspiring Residential & Commercial Spaces</h4>
        <div class="row">
            <div class="col-6">
                <button>EXPLORE RECENT WORK</button>
            </div>
            <div class="col-6">
                <button>GET A QUOTE TODAY</button>
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
        h4{
            color: #f9d03f;
        }
    }
</style>