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
                <div class="col">
                    <h6>LATEST TWEETS</h6>
                    <TweetComponent v-for="(tweet, index) in tweets" :key="index" 
                    :userName="tweet.userName" 
                    :profileImage="tweet.profileImage" 
                    :postTime="tweet.postTime"/>
                </div>
                <div class="col">
                    <h6>CONTACT US TODAY</h6>

                </div>
                <div class="col">
                    <h6>FIND US</h6>

                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import TweetComponent from './TweetComponent.vue';
    export default {
    name: "FooterComponent",
    data(){
        return{
            tweets: [
                {
                    userName: 'Theme Fusion',
                    profileImage: '3a74ce3d0532b7773b174c45ca3bd05a_normal.png',
                    postTime: '22'
                }
            ]
        }
    },
    components: { TweetComponent }
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
            background-color: #1e1e1e;
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
                    h6{
                        color: #f9d03f;
                        font-weight: bold!important;
                    }
                    
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