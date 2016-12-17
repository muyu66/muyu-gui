<template>
    <div class="index">
        <swiper :options="swiperOption" style="height: 100%">
            <swiper-slide>
                <h1 v-for="todo in todos" class="text-center">{{ todo.text1 }}
                    <small>{{ todo.text2 }}</small>
                </h1>
            </swiper-slide>
            <swiper-slide>
                <h1 class="text-center">Official website is building
                    <small>有朋自远方来，不亦乐乎</small>
                </h1>
            </swiper-slide>
            <swiper-slide>
                <h1 class="text-center">Coding
                    <small>星际的远征 StatLongWaric</small>
                </h1>
            </swiper-slide>
            <swiper-slide>
                <h1 class="text-center">Planing
                    <small>星际议会</small>
                </h1>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    import {swiper, swiperSlide} from 'vue-awesome-swiper'

    export default {
        name: 'index',
        data () {
            return {
                todos: [
                    {
                        text1: 'Learn JavaScript',
                        text2: 'Learn JavaScript'
                    },
                    {
                        text1: 'Learn JavaScript',
                        text2: 'Learn JavaScript'
                    },
                    {
                        text1: 'Learn JavaScript',
                        text2: 'Learn JavaScript'
                    },
                ],
                swiperOption: {
                    pagination: '.swiper-pagination',
                    direction: 'vertical',
                    slidesPerView: 1,
                    paginationClickable: true,
                    spaceBetween: 30,
                    mousewheelControl: true,
                    autoHeight: true
                }
            }
        },
        components: {
            swiper,
            swiperSlide
        }
    }
</script>

<style scoped>
    .index {
        background-color: rgb(223, 84, 32);
        height: 100%;
        line-height: 100%;
        width: 100%;
        color: white;
    }

    h1 {
        padding-top: 18%;
    }

    small {
        color: #c9d0d6;
    }
</style>
