<template>
    <div class="index">
        <swiper :options="swiperOption" style="height: 100%">
            <div id='right'>
                <button type="button" class="btn btn-warning">Stable</button>
                <button type="button" class="btn btn-warning">Rolling</button>
            </div>
            <swiper-slide v-for="title in titles">
                <h1 class="slide text-center">{{ title.main_title }}
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
                        main_title: 'Building',
                        sub_title: '有朋自远方来，不亦乐乎'
                    },
                    {
                        main_title: 'Coding',
                        sub_title: '星际的远征'
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
                    paginationClickable: false,
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
        position: relative;
        height: 100%;
        width: 100%;
        color: white;
        background-color: rgb(223, 84, 32);
    }

    .slide {
        position: relative;
        top: 40%;
        transform: translateY(-50%);
    }

    small {
        color: #c9d0d6;
    }

    #right {
        position: absolute;
        right: 1%;
        top: 1%;
    }
</style>
