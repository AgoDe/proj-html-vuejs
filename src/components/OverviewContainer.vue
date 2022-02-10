<template>
    <div class="overview">
        <div class="container">

            <!-- info (first child) -->
            <div>
                <div>
                    <div class="button active">Overview</div>
                    <div class="button">Our Mission</div>
                </div>

                <div class="special-text">Our philosophy is learning through play as we offer a stimulating environment for children</div>

                <div>
                    <div class="info-box">
                        <div class="round-box">
                            <img src="../assets/clock_alt.png" alt="clock">
                        </div>
                        <div class="info">
                            <h4>Full Day Sessions</h4>
                            <p>Pulvinar est metro ligula blandit maecenas retrum gravida cuprum. Maecenas node estibulum.</p>
                        </div>
                    </div>
                    <div class="info-box">
                        <div class="round-box">
                            <img src="../assets/diagram_alt.png" alt="clock">
                        </div>
                        <div class="info">
                            <h4>Varied Classes</h4>
                            <p>Pulvinar est metro ligula blandit maecenas retrum gravida cuprum. Maecenas node estibulum.</p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- end of info (first child) -->

            <!-- img slider (last child) -->
            <div>
                <div class="img-slider">
                    <img src="/images/overview_3.jpg" alt="">
                    <div class="slider-button prev"> 
                        <img src="../assets/slider_previous.png" alt="prev-chevron">
                    </div>
                    <div class="slider-button next"> 
                        <img src="../assets/slider_next.png" alt="prev-chevron">
                    </div>
                </div>

                <div class="img-container">
                    <div class="img-box">
                        <img src="/images/overview_1.jpg" alt="">
                    </div>
                    <div class="img-box">
                        <img src="/images/overview_2.jpg" alt="">
                    </div>
                    <div class="img-box">
                        <img src="/images/overview_3.jpg" alt="">
                    </div>
                </div>
            </div>
            <!-- end of img slider (last child) -->


        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

    .overview {
        background: $light-grey;
        
        .container {
            padding: 30px 0;
            display: flex;
            align-items: center;

            &>div {
                width: 50%;
                padding: 10px;
                text-align: left;
                
            }
            &>div:first-child {

                .button {
                    margin: 4px;
                    color: $grey;
                    box-shadow: 0 0 2px  $grey;
                }
                .button.active {
                    background: $orange;
                    color: $sugar;
                    position: relative;

                    &::after{
                        content: '';
                        width: 0;
                        height: 0;
                        line-height: 0px;
                        border-top: 12px solid $orange;
                        border-left: 12px solid transparent;
                        border-right: 12px solid transparent;
                        position: absolute;
                        bottom: -6px;
                        left: 50%;
                        transform:translate(-50%, 0);
                    }
                }

                .special-text {
                    margin: 15px 0;
                }
                .info-box {      
                    display: flex;
                    align-items: center;

                    .round-box {
                        background-color: $orange;
                    }
                    .info {
                        width: 80%;
                        padding-left: 15px;
                        margin: 10px;

                        h4 {
                            color: $purple;
                            margin: 6px 0 ;
                            font-size: 14px;
                        }
                        p {
                            color: $grey;
                            font-size: 11px;
                        }
                    }
                }

            } // end of first-child
            &>div:last-child {
                .img-slider {
                    width: 100%;
                    position: relative;
                    img {
                        width: 100%;
                    }
                    .slider-button {
                        height: 40px;
                        width: 40px;
                        background: $orange;
                        cursor: pointer;

                        position: absolute;
                        top: 50%;

                        &:hover {
                            background: $purple;
                        }
                    }
                    .slider-button.prev {
                        left: 0;
                    }
                    .slider-button.next {
                        right: 0;
                    }
                }
                .img-container {
                    width: 100%;
                    display: flex;
                    justify-content: space-between;

                    .img-box {
                        width: calc(95% / 3);
                        img {
                            width: 100%;
                            height: 100%;
                            object-fit: cover;
                        }
                    }
                }

            } // end of last-child


        }
    }
</style>