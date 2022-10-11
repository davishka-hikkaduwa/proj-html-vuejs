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
                    <div class="heading-container">
                        <h6>LATEST TWEETS</h6>
                    </div>
                    <TweetComponent class="tweet-container" v-for="(tweet, index) in tweets" :key="index" 
                    :userName="tweet.userName" 
                    :profileImage="tweet.profileImage"
                    :tweetContent="tweet.tweetContent" 
                    :postTime="tweet.postTime"/>
                </div>
                <div class="col">
                    <div class="heading-container">
                        <h6>CONTACT US TODAY</h6>
                    </div>
                    <ContactsComponent/>
                </div>
                <div class="col">
                    <div class="heading-container">
                        <h6>FIND US</h6>
                    </div>
                    <div class="map-container">
                        <img src="@/assets/img/construction_map_pin.png" alt="map">
                    </div>
                </div>
            </div>
        </div>
        <SocialsComponent/>
    </footer>
</template>

<script>
import TweetComponent from './TweetComponent.vue';
import ContactsComponent from './ContactsComponent.vue';
import SocialsComponent from './SocialsComponent.vue';
    export default {
    name: "FooterComponent",
    data(){
        return{
            tweets: [
                {
                    userName: 'Theme Fusion',
                    profileImage: '3a74ce3d0532b7773b174c45ca3bd05a_normal.png',
                    postTime: 22,
                    tweetContent: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit illum ut quasi ipsa error natus maxime dicta dolorum.'
                }
            ]
        }
    },
    components: { 
        TweetComponent, 
        ContactsComponent, 
        SocialsComponent 
    }
}     

</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

    footer{
        .bar{
            height: 10px;
            background-color: $dove-grey-color;
        }
        .container-fluid{
            padding: 50px 0;
            background-color: $cod-grey-color;
            display: flex;
            flex-direction: column;
            justify-content: center;
            color: $white-color;
            // height: 300px;
            .row{
                padding: 0 50px;
                height: 100%;

                .col{
                    height: 100%;    
                    margin: 0 5px;
                    .heading-container{
                        margin-bottom: 20px;

                        h6{
                        color: $bright-sun-color;
                        font-weight: bold!important;
                    }
                    }
                    
                    .tweet-container{
                    }
                    .map-container{
                        width: 100%;
                        img{
                            width: 100%;
                        }
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
                        color:$dove-grey-color;
                    }
                    .gold-btn{

                    }
                    .gold-btn:hover{
                        background-color: $bright-sun-color!important;
                    }
                }
            }
        }
        
    }
</style>