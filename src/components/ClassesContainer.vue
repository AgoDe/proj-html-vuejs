<template>
    <div class="container padding-y30">
        
        <h2>Our Classes</h2>
        <div class="subtitle">
            Our preschool program has four dedicated classes
        </div>
        <img class="divider" src="../assets/header_divider.png" alt="">

        <div class="presentation">
            <div class="special-text">
                We provided four classes with nine to twenty children each aged twelve month to five years of age
            </div>
            <div class="description-text">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt fugiat error et quia corporis inventore illum nihil reiciendis. Optio architecto dolor recusandae accusantium ea quibusdam? Libero totam explicabo ullam eligendi.
            </div>
        </div>

        <div class="classes">

            <div 
            class="class-box"
            v-for="(item, index) in classes"
            :key="index"
            >
                <!-- left side -->
                <div>
                    <h3>{{item.title}}</h3>
                    <h4>{{item.class_name}}</h4>
                    <div class="info">
                        <div>
                            <div class="item-data">{{item.old}}</div>
                            <div class="item-title">{{item.old_measure}}</div>
                        </div>

                        <div>
                            <div class="item-data">{{item.class_size}}</div>
                            <div class="item-title">Class size</div>
                        </div>
                    </div>
                </div>
                
                <!-- right side -->
                <div>
                    <img :src="`/images/${item.path}`" :alt="item.path">
                    <div class="button special orange">read more</div>
                </div>
            </div> <!-- end of class-box -->
        </div> <!-- end of classes -->

    </div>
</template>

<script>
export default {
    data() {
        return {
            classes: [
                {
                    title: 'Little Lambs',
                    class_name: 'Class Name',
                    old: '12-24',
                    old_measure: 'Month Old',
                    class_size: '9',
                    path: 'class_01.jpg',
                },
                {
                    title: 'Bouncy Bears',
                    class_name: 'Class Name',
                    old: '2-3',
                    old_measure: 'Year olds',
                    class_size: '12',
                    path: 'class_02.jpg',
                },
                {
                    title: 'Tenderhearts',
                    class_name: 'Class Name',
                    old: '3-4',
                    old_measure: 'Year olds',
                    class_size: '15',
                    path: 'class_03.jpg',
                },
                {
                    title: 'Shining Stars',
                    class_name: 'Class Name',
                    old: '4-5',
                    old_measure: 'Year olds',
                    class_size: '20',
                    path: 'class_04.jpg',
                },
            ]
        }
    }
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

.container {
    .presentation {
        display: flex;

        div {
            padding: 10px;
            width: 50%;
            text-align: justify;
        }
    } // end of presentation

    .classes {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        

        .class-box {
            margin: 1px solid black;
            width: calc(50% - 15px);
            height: 200px;
            padding: 15px 0 ;
            display: flex;

            &>div {
                width: 50%;
                color: $sugar;
            }
            &>div:first-child {
                background: $purple;
                text-align: left;
                padding: 15px;
                position: relative;

                h3 {
                    font-weight: 500;
                }
                h4 {
                    color: $light-grey;
                    font-size: 11px;
                    font-weight: 500;
                    margin-top: 5px;
                }
                .info {
                    display: flex;
                    position: absolute;
                    bottom: 10px;
                    left: 10px;
                    width: 90%;
                    
                    &>div:first-child {
                        border-right: 1px $sugar solid;
                    }
                    &>div {
                        width: 50%;
                        text-align: center;
                        font-size: 13px;
                        font-weight: 500;

                        .item-title {
                            color: $light-grey;
                        }
                        
                    }
                }
            } // end of first-child
            &>div:last-child {
                position: relative;
                
                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }
                .button {      
                    position: absolute;
                    right: 0;
                    bottom: 0;
                }
            }

        }
    } // end of classes
} // end of container

</style>