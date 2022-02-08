<template>
    <main>
        

        <div class="jumbotron">
            <div class="container">


            </div>
        </div>

        <div class="banner">
            <div class="container">
                <p>How to Enroll Your Child to a Class?</p>
                <div class="button">learn more</div>
            </div>
        </div>



      
    </main>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';
    main {
        

        .jumbotron {
            
           
            
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
                }
            }
        } // end of banner
    } 
       

</style>