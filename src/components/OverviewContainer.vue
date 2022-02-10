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
                    <img :src="`/images/${activeImage}`" alt="">
                    <div @click="sliderPrev" class="slider-button prev"> 
                        <img src="../assets/slider_previous.png" alt="prev-chevron">
                    </div>
                    <div @click="sliderNext" class="slider-button next"> 
                        <img src="../assets/slider_next.png" alt="prev-chevron">
                    </div>
                </div>

                <div class="img-container">
                    <div 
                    class="img-box" 
                    :class="{active : img.status}"
                    v-for="(img, index) in sliderImages" 
                    :key="index"
                    @click="clickForOn(img)"
                    >
                        <img :src="`/images/${img.path}`" alt="">
                    </div>
                </div>
            </div>
            <!-- end of img slider (last child) -->


        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            imageIndex: 0,
            sliderImages: [
                {   
                    index: 0,
                    path:'overview_1.jpg',
                    status: true,
                },
                {   
                    index: 1,
                    path:'overview_2.jpg',
                    status: false,
                },
                {   
                    index: 2,
                    path:'overview_3.jpg',
                    status: false,
                },
            ],
        }
    },
    computed: {
        activeImage: function() {
            this.imageOn()
            return this.sliderImages[this.imageIndex].path
        }
    },
    methods: {
        sliderNext: function() {
            this.imageIndex < this.sliderImages.length -1 ? this.imageIndex++ : this.imageIndex = 0
        },
        sliderPrev: function() {
            this.imageIndex <= 0 ? this.imageIndex = this.sliderImages.length -1 : this.imageIndex--
        },
        imageOn: function() {
             this.sliderImages.forEach(el => {
                el.status = false
            });
            this.sliderImages[this.imageIndex].status = true;
        },
        clickForOn: function(img) {
            this.imageIndex = img.index
        }
        
    }
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
                    height: 275px;
                    width: 100%;
                    position: relative;

                    img {
                        width: 100%;
                        object-fit: contain;
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
                        padding: 10px 0;
                        width: calc(100% / 3 - 5px);
                        cursor: pointer;
                        border-bottom: transparent 2px solid;
                        img {
                            width: 100%;
                            height: 100%;
                            object-fit: cover;
                        }
                    }
                    .img-box.active {
                        border-color: $orange;
                    }
                }

            } // end of last-child


        }
    }
</style>