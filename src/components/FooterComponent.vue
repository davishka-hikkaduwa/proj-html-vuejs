<template>
    <footer>
        <div class="bar"></div>
        <div class="container-fluid">
            <div class="row">
                <div class="col">
                    <div class="image-container">
                        <img src="@/assets/img/footer-logo.png" alt="logo">
                    </div>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus placeat blanditiis in consequatur, earum, corporis.</p>
                    <button class="gold-btn">LEARN MORE</button>
                </div>
                <div class="col"></div>
                <div class="col"></div>
                <div class="col"></div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponent',
    }     

</script>

<style scoped lang="scss">
    footer{
        .bar{
            height: 10px;
            background-color: #6b6868;
        }
        .container-fluid{
            padding: 50px 0;
            background-color: #31312f;
            display: flex;
            flex-direction: column;
            justify-content: center;
            color: #fff;
            // height: 300px;
            .row{
                padding: 0 50px;
                height: 100%;

                .col{
                    border: 1px solid white;
                    height: 100%;
                    // height: 200px;
                    
                    margin: 0 5px;
                    
                }
                .col:first-child{
                    .image-container{
                        margin: 10px 0;
                        height: 80px;
                        img{
                            height: 70%;
                        }                    
                    }
                    p{
                        margin: 10px 0;
                        color:#6b6868;
                    }
                    .gold-btn{

                    }
                    .gold-btn:hover{
                        background-color: #f9d03f!important;
                    }
                }
            }
        }
    }
</style>