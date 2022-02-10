<template>
    <div class="goals-container">
        <div class="container">

            <!-- first child -->
            <div>
                <div class="special-text">
                    We have benn educating children for over fifteen years. Our goal is to create a place that engages each child.
                </div>
                <div class="description-text">
                    Praesent arcu gravida vehicula est node maecenas loareet morbi a dosis luctus. Urna eget lacinia eleifend luctus a arcu quis facilisis veneratis aenean interdum.
                </div>

                <ul>
                    <li>Comprensive reporting on individual achievements</li>
                    <li>Educational field trips and school presentations</li>
                    <li>Individual attention in a small-class setting</li>
                    <li>Learning program with after-school care</li>
                    <li>Opportunies to carry out scientific investigations</li>
                    <li>Positive learnign environment for your child</li>
                </ul>
                    
            </div>
            <!-- end of first child -->

            <!-- last child -->
            <div>
                <div class="goal-box">
                    <div class="round-box">
                        <img src="../assets/toy.png" alt="train">
                    </div>

                    <div class="special-text">Learning & Fun</div>
                    <div class="description-text">Peaesent modea est gravida node vehicula luctus</div>
                </div>

                <div class="goal-box">
                    <div class="round-box">
                        <img src="../assets/meal.png" alt="meal">
                    </div>

                    <div class="special-text">Healty Meals</div>
                    <div class="description-text">Terminal interdum a eleifend maecenas est morbi</div>
                </div>

                <div class="goal-box">
                    <div class="round-box">
                        <img src="../assets/school.png" alt="school">
                    </div>

                    <div class="special-text">Friendly Place</div>
                    <div class="description-text">Peaesent modea est gravida node vehicula luctus</div>
                </div>

                <div class="goal-box">
                    <div class="round-box">
                        <img src="../assets/shield.png" alt="shield">
                    </div>

                    <div class="special-text">Children Safety</div>
                    <div class="description-text">Terminal interdum a eleifend maecenas est morbi</div>
                </div>
            </div>
            <!-- end of last child -->

        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';
    .goals-container {
        background: $light-grey;
        padding: $container-pad 0;

        .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            &>div {
                width: calc(50% - 15px);
                padding: 15px 0;
                text-align: left;

            }
            &>div:first-child {
                .special-text {
                    margin-bottom: 15px;
                }
                .description-text {
                    margin-bottom: 15px;
                }
                ul {
                    list-style: none;

                    li {
                        font-size: 11px;
                        color: $grey;
                        position: relative;
                        margin: 4px;
                        padding-left: 15px;
                        vertical-align: middle;

                        &::before {
                            position: absolute;
                            content: ' '; 
                            left: 0;
                            top: 1.5px;
                            width: 10px;
                            height: 10px;
                            background: url(../assets/style_1.png);
                            background-size: contain;
                        }
                    }
                }
            } // end of fisrt-child
            &>div:last-child {
                display: flex;
                flex-wrap: wrap;

                .goal-box {
                    padding: 10px 0;
                    width: calc(50% - 10px);
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    text-align: center;

                    .round-box {            
                        background: $sugar;
                    }
                    .special-text {
                        margin: 10px;
                    }
                }
            } // end of last-child
        }

    }

</style>
