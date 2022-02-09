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

                    <div class="button">buy this theme now</div>

                </div>


            </div>
        </div>
        <!-- end of jumbotron -->


        <div class="banner">
            <div class="container">
                <p>How to Enroll Your Child to a Class?</p>
                <div class="button">
                    learn more 
                </div>
            </div>
        </div>

        <!-- welcome to fable -->
        <div class="welcome container">

            <h2>Welcome to Fable</h2>
            <div class="subtitle">
                Fable daycare, preshool and kindergarten
            </div>
            <img class="divider" src="../assets/header_divider.png" alt="">

            <div class="services">

                <div class="service-box">
                    <div class="round-box">
                        <img src="../assets/schoolbag_alt.png" alt="schoolbag">
                    </div>

                    <h4>Morbi Etos</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="round-box purple">
                        <img src="../assets/stroller_alt.png" alt="schoolbag">
                    </div>

                    <h4>Congue Gravida</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="round-box">
                        <img src="../assets/globe_alt.png" alt="schoolbag">
                    </div>

                    <h4>Maecenas Node</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est enim itaque quibusdam excepturi maxime provident voluptatum ipsa eius ratione. Excepturi nam, minus sequi ea possimus quia facilis et eum ratione?</p>
                </div>
                <div class="service-box">
                    <div class="round-box purple">
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
        <!-- end of media-gallery -->

        <!-- news-container -->
        <!-- end of news-container -->




      
    </main>
</template>

<script>
import ClassesContainer from './ClassesContainer.vue'
import GoalsContainer from './GoalsContainer.vue'
import OverviewContainer from './OverviewContainer.vue'

export default {
  components: { 
    ClassesContainer,
    OverviewContainer,
    GoalsContainer },
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';
    main {
        

        .jumbotron {
            
            background-image: url('../assets/slider_slide2_background.png');
            background-size: contain;
            
            .container {
                height: 400px;
                display: flex;
                align-items: center;

                .jumbo-box {
                    color: $purple;

                    .text-special {
                        color: $orange;
                        font-family: 'Satisfy', cursive;
                        padding: 7px 0;
                        font-size: 22px;
                    }
                    h1 {
                        font-size: 28px;
                        font-weight: bold;
                    }
                    p {
                        font-size: 28px;
                        padding: 6px 0 ;
                    }
                    .button {
                        margin-top: 14px;
                        background: $orange;
                        color: $sugar;
                        width: 130px;
                        
                          
                        &:hover {
                        background-color: $purple;
                        }
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
                    font-size: 19px;
                }
                .button {
                    border: white 1px solid;

                    img {
                        height: 25px;
                    }

                     &:hover {
                        background-color: $sugar;
                        color: $purple;
                    }
                }
            }// end of container
        } // end of banner

        .welcome {
            padding: $container-pad 0;
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

                    .round-box {
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
                    .round-box.purple {
                        background: $purple;
                    }
                     h4 {
                        color: $purple;
                    }
                    p {
                        font-size: 10px;
                    }
                }
            }
        } // end of welcome
    } 
       

</style>