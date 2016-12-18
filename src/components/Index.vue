<template>
    <div class="index">
        <swiper :options="swiperOption" style="height: 100%">
            <swiper-slide v-for="title in titles">
                <h1 class="text-center">{{ title.main_title }}
                    <small>{{ title.sub_title }}</small>
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
                titles: [
                    {
                        main_title: 'Official website is building',
                        sub_title: '有朋自远方来，不亦乐乎'
                    },
                    {
                        main_title: 'Coding',
                        sub_title: '星际的远征 StatLongWaric'
                    },
                    {
                        main_title: 'Planing',
                        sub_title: '星际议会'
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
        display: flex;
        justify-content: center;
        color: white;
        background-color: rgb(223, 84, 32);
        align-items: center;
    }

    small {
        color: #c9d0d6;
    }
</style>
