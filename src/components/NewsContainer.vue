<template>
    <div class="container padding-y30">

        <h2>What's New</h2>
        <div class="subtitle">
            Keep up to date with the latest news
        </div>
        <img class="divider" src="../assets/header_divider.png" alt="">

        <div class="news-container padding-y30">

            <div 
            class="news-box"
            v-for="(item, index) in news"
            :key="index"
            >
                <div class="description-text"> {{item.date.month}} {{item.date.day}}, {{ item.date.year}} </div>

                <img :src="`/images/${item.path}`" alt="blog">

                <h4>{{item.title}}</h4>

                <div class="description-text">
                    {{item.description}}
                </div>

                <div>
                    <span>
                        <img src="/images/author.png" alt="author">
                        {{item.author}}
                    </span>
                    <span>
                        <img src="/images/category.png" alt="author">
                        {{item.category}}, {{item.type}}
                    </span>
                </div>
            </div>

        </div> <!-- end of news-container -->

        <div class="button special orange">go to blog</div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            news: [
                {
                    date: {
                        day: '03',
                        month: 'October',
                        year: '2014',
                    },
                    path:'blog_08.jpg',
                    title: 'Drawing and Painting Lesson',
                    description: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum',
                    author: 'Anna Brown',
                    category:'Events',
                    type: 'Fun',
                    number: '42'
                },
                {
                    date: {
                        day: '03',
                        month: 'October',
                        year: '2014',
                    },
                    path:'blog_10.jpg',
                    title: 'Fall Parents Meeting Day',
                    description: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum',
                    author: 'Anna Brown',
                    category:'Dance',
                    type: 'Education',
                    number: '19'
                },
                {
                    date: {
                        day: '20',
                        month: 'September',
                        year: '2014',
                    },
                    path:'blog_09.jpg',
                    title: 'Birthday in Kindergarten',
                    description: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum',
                    author: 'Anna Brown',
                    category:'Games',
                    type: 'General',
                    number: '22'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

    .news-container {
        display: flex;
        justify-content: space-between;

        .news-box {
            width: calc(100% / 3 - 10px);
            text-align: left;

            img {
                width: 100%;
            }
            h4 {
                color: $purple;
                margin: 10px 0;
            }
            .description-text {
                padding-bottom: 15px;
                border-bottom: 1px $light-grey solid;
            }

            span {
                margin-right: 6px;
                color: $grey;
                font-weight: 500;
                font-size: 9px;

                img {
                    vertical-align: middle;
                    height: 10px;
                    width: 10px;
                    margin: 3px;
                }
            }
        }

    }

</style>