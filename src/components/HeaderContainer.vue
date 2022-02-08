<template>
    <header>
        <div class="container"> 

            <img  class="logo" src="../assets/images/logo.png" alt="logo">

            <ul>
                <li
                :class="{active : item.active}"
                v-for="(item, index) in navItem"
                :key="index"
                >
                    <img v-if="item.active" :src="`/images/${item.pathActive}`" :alt="item.item">
                    <img v-if="!(item.active)" :src="`/images/${item.path}`" :alt="item.item">
                    <div> {{item.item}} </div>
                </li>
            </ul>

        </div>
    </header>
</template>

<script>
export default {
    props: {
        navItem: Array,
    }
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

    header {

        .container {
            height: 80px;
            display: flex;
            justify-content: space-between;

            .logo {
                height: 100%;
        }
        
        ul {
            height: 100%;
            list-style: none;
            display: flex;
        

            li {
                height: 100%;
                width: 75px;
                color: $purple;
                cursor: pointer;
                
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;

                img {
                    height: 35px;
                    padding-bottom: 10px;
                }
                div {
                    font-size: 12px;
                    
                }
            }
            li.active {
                background-color: $orange;
                color: $sugar;
            }
        }
    
        } // end of container
    } // end of header


</style>