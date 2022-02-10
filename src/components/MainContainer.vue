<template>
    <main>
        
        <!-- jumbotron -->
        <div class="jumbotron">
            <div class="container">
                <div class="jumbo-box">

                    <div class="text-special">
                        Friendly Atmosphere
                    </div>
                    <h1>Welcoming Place</h1>
                    <p>For Every Child</p>

                    <div class="button orange">buy this theme now</div>

                </div>

            </div>
        </div>
        <!-- end of jumbotron -->


        <div class="banner">
            <div class="container">
                <p>How to Enroll Your Child to a Class?</p>
                <div class="button special white">
                    learn more 
                </div>
            </div>
        </div>

        <!-- welcome to fable -->
        <div class="welcome container padding-y30">

            <h2>Welcome to Fable</h2>
            <div class="subtitle">
                Fable daycare, preshool and kindergarten
            </div>
            <img class="divider" src="../assets/header_divider.png" alt="">

            <div class="services">

                <div class="service-box">
                    <div class="roundbox">
                        <img src="../assets/schoolbag_alt.png" alt="schoolbag">
                    </div>

                    <h4>Morbi Etos</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="roundbox purple">
                        <img src="../assets/stroller_alt.png" alt="schoolbag">
                    </div>

                    <h4>Congue Gravida</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="roundbox">
                        <img src="../assets/globe_alt.png" alt="schoolbag">
                    </div>

                    <h4>Maecenas Node</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="roundbox purple">
                        <img src="../assets/bell_alt.png" alt="schoolbag">
                    </div>

                    <h4>Praesent Morbi</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>

            </div>
            
        </div>
        <!-- end of welcome to fable -->

        <!-- overview -->
        <overview-container/>
        <!-- end of overview -->

        <!-- classes-container -->
        <classes-container/>
        <!-- end of classes-container -->

        <!-- goals-container -->
        <goals-container/>
        <!-- end of goals-container -->

        <!-- media-gallery -->
        <div class="gallery">
            <div>
                <img src="../assets/gallery_01.jpg" alt="gallery-1">
            </div>
            <div>
                <img src="../assets/gallery_02.jpg" alt="gallery-2">
            </div>
            <div>
                <img src="../assets/gallery_03.jpg" alt="gallery-3">
            </div>
            <div>
                <img src="../assets/gallery_04.jpg" alt="gallery-4">
            </div>
        </div>
        <!-- end of media-gallery -->

        <!-- special banner -->
        <div class="banner special">
            <div class="container">
                <p>See Our Kindergarten Photo Gallery!</p>
                <div class="button special white">
                    view gallery
                </div>
            </div>
        </div>
        <!-- end of special banner -->

        <!-- reviews -->
        <reviews-container/>
        <!-- end of reviews -->

        <!-- news-container -->
        <news-container/>
        <!-- end of news-container -->




      
    </main>
</template>

<script>
import ClassesContainer from './ClassesContainer.vue'
import GoalsContainer from './GoalsContainer.vue'
import NewsContainer from './NewsContainer.vue'
import OverviewContainer from './OverviewContainer.vue'
import ReviewsContainer from './ReviewsContainer.vue'

export default {
  components: { 
    ClassesContainer,
    OverviewContainer,
    GoalsContainer,
    ReviewsContainer,
    NewsContainer },
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';
    main {

        .jumbotron {         
            background: 
                url('../assets/slider_slide2_img1.png') no-repeat 60%, 
                url('../assets/slider_slide2_img2.png') no-repeat 80%, 
                url('../assets/slider_icon10.png') no-repeat 30% 5%,
                url('../assets/slider_icon14.png') no-repeat 36% 20%,
                url('../assets/slider_icon11.png') no-repeat 40% 5%,
                url('../assets/slider_icon12.png') no-repeat 44% 25%,
                url('../assets/slider_icon13.png') no-repeat 50% 10%,
                url('../assets/slider_slide2_background.png') repeat
                ;
                 background-size: contain, contain, 4% 16%, 3% 10%, 4% 13%, 5% 15%, 5% 15%, contain;

            .container {
                height: 400px; 
                display: flex;
                align-items: center;

                .jumbo-box {
                    text-align: left;
                    color: $purple;

                    .text-special {
                        color: $orange;
                        font-family: 'Satisfy', cursive;
                        padding: 7px 0;
                        font-size: 25px;
                    }
                    h1 {
                        font-size: 34px;
                        font-weight: bold;
                    }
                    p {
                        font-size: 34px;
                        padding: 6px 0 ;
                    }
                }
            }
            
           
            
        } // end of jumbotron
        .banner {
            background: $purple;
            color: $sugar;
            
            .container {
                height: 70px;
                display: flex;
                justify-content: space-between;
                align-items: center;

                p {
                    font-size: 20px;
                }
                
            }// end of container
        } // end of banner
        .banner.special {
            background: url(../assets/pattern.png) repeat;
            background-size: cover;
        }
        .welcome {
            text-align: center;

            .services {
                padding-top: 20px;
                display: flex;
                justify-content: space-between;

                .service-box {
                    width: 180px;
                    height: 300px;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    align-items: center;

                    .roundbox {
                        height: 150px;
                        width: 150px;
                        border-radius: 50%;
                        background: $orange;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        img {
                            height: 60px;
                            vertical-align: middle;
                        }
                    }
                    .roundbox.purple {
                        background: $purple;
                    }
                     h4 {
                        color: $purple;
                    }
                    p {
                        font-size: 10px;
                        text-align: justify;
                    }
                }
            }
        } // end of welcome
        .gallery {
            display: flex;
             
            div {
                width: calc(100% / 4);
                position: relative;
                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }
                &:hover::after {
                    content: '';
                    width: 120px;
                    height: 120px;
                    border-radius: 50%;
                    background: $purple url(../assets/image_overlay.png) no-repeat center;
                    opacity: 0.6;
                    position: absolute;
                    z-index: 1001;
                    left: 50%;
                    top: 50%;
                    transform: translate(-50%, -50%);
                }
            }
        } // end of gallery
    } 
       

</style>