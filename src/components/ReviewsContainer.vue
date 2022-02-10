<template>
    <div class="reviews">
        <div class="container">

            <div class="round-box">
                <img src="../assets/quote_alt.png" alt="quote">
            </div>

            <h3>I have to say that 2 children ages 5 and 2 and have used various daycare's in Kindergartens and this is by far the very best I have ever used</h3>

            <div class="border-rule"></div>

            <p>Cecil J. Kirk</p>

        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

    .reviews {
        background: url(../assets/parallax_02.jpg);
        background-size: cover;
        background-position: center ;

        .container {
            color: $sugar;
            text-align: center;
            height: 360px;

            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;

            .round-box {
                border: 1px $sugar solid;
                margin: 20px;
            }
            h3 {
                font-size: 22px;
                margin: 20px;
            }
            p {
                font-size: 12px;
            }
        } // end of container
    }
</style>