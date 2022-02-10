<template>
    <div class="overview">
        <div class="container padding-y30">

            <!-- info (first child) -->
            <div>
                <div class="button-box">
                    <div 
                    class="button"
                    :class="{active : item.status}"
                    v-for="(item, index) in navItems"
                    :key="index"
                    @click="activeNavItem(item)"
                    >
                    {{item.item}}
                    </div>    
                </div>

                <div class="overview" v-if="navItems[0].status">
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

                <div class="our-mission" v-if="navItems[1].status">
                    <img src="data:image/jpeg;base64,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" alt="">
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
            navItems: [
                {
                    item: '0verview',
                    status: true,
                },
                {
                    item: 'our Mission',
                    status: false,
                },
            ],
            imageIndex: 0,
            sliderImages: [
                {   
                    index: 0,
                    path:'overview_1.jpg',
                    status: false,
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
        activeNavItem: function(item) {
            this.navItems.forEach(element => {
                element.status = false
            });
            item.status = true
        },
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
            display: flex;
            justify-content: space-between;
            align-items: center;

            &>div {
                width: 48%;
                text-align: left; 
            }
            &>div:first-child {
                position: relative;
                height: 300px;

                .button-box {
                    position: absolute;
                    top: -40px;

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

                .our-mission {
                    width: 100%;
                    height: 100%;
                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
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
        } // end of container
    } // end of overview
</style>