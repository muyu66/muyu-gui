<template>
    <div class="hello">
        <swiper :options="swiperOption" style="height: 100%">
            <swiper-slide>
                <h1 class="text-center">Muyu 官网正在建设中
                    <small>有朋自远方来，不亦乐乎</small>
                </h1>
            </swiper-slide>
            <swiper-slide>
                <h1 class="text-center">星际的远征 StatLongWaric
                    <small>正在开发中</small>
                </h1>
            </swiper-slide>
            <swiper-slide>
                <h1 class="text-center">议会 - 星际分会场
                    <small>正在开发中</small>
                </h1>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    import {swiper, swiperSlide} from 'vue-awesome-swiper'

    export default {
        name: 'hello',
        data () {
            return {
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
    .hello {
        background-color: rgb(223, 84, 32);
        height: 100%;
        width: 100%;
        color: white;
        margin: 0 auto;
    }
</style>
