<template>
    <div class="hello">
        <swiper :options="swiperOption" style="height: 100%">
            <swiper-slide><div>有朋自远方来，不亦乐乎</div></swiper-slide>
            <swiper-slide><div>星际的远征 StatLongWaric</div></swiper-slide>
            <swiper-slide><div>议会 - 星际分会场</div></swiper-slide>
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
        margin: auto;
    }
</style>
