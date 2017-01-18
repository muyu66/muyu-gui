<template>
    <div class="index">
        <swiper :options="swiperOption" style="height: 100%">
            <div class='right'>
                <button type="button" class="btn btn-danger ubuntu" @click="go_url">
                    {{ reverseVersion() }}
                </button>
            </div>
            <swiper-slide v-for="title in titles" v-bind:style='title.theme'>
                <button v-if="title.sub_title == '星际的远征'" type="button"
                        class="btn btn-default right" @click="goSlwRolling">2.0.0 Alpha1
                </button>
                <h1 class="h1 text-center">{{ title.main_title }}
                    <small :style='title.theme_small'>{{ title.sub_title }}</small>
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
        methods: {
            isRolling: function () {
                let hostName = window.location.hostname;
                return hostName === 'rolling.muyu.party';
            },
            reverseVersion: function () {
                if (this.isRolling()) {
                    return '稳定版';
                }
                else {
                    return '实时推进';
                }
            },
            go_url: function () {
                if (this.isRolling()) {
                    window.location.href = 'https://www.muyu.party';
                }
                else {
                    window.location.href = 'https://rolling.muyu.party';
                }
            },
            goSlwRolling: function () {
                window.location.href = 'https://rolling.starlongwaric.space';
            },
        },
        data()
        {
            return {
                titles: [
                    {
                        main_title: 'Building',
                        sub_title: '有朋自远方来，不亦乐乎',
                        theme: {
                            color: 'white',
                            backgroundColor: 'rgb(223, 84, 32)',
                        },
                        theme_small: {
                            color: '#E2EBF1',
                        },
                    },
                    {
                        main_title: '2.0.0 Alpha1',
                        sub_title: '星际的远征',
                        theme: {
                            color: 'white',
                            backgroundColor: '#333',
                        },
                        theme_small: {
                            color: '#c9d0d6',
                        },
                    },
                    {
                        main_title: 'Planing',
                        sub_title: '问仙之志',
                        theme: {
                            color: 'white',
                            backgroundColor: '#1786aa',
                        },
                        theme_small: {
                            color: '#ccc',
                        },
                    },
                    {
                        main_title: 'Planing',
                        sub_title: '星际议会',
                        theme: {
                            color: 'black',
                            backgroundColor: '#a6f2bf',
                        },
                        theme_small: {
                            color: '#4b4b4b',
                        },
                    },
                ],
                swiperOption: {
                    pagination: '.swiper-pagination',
                    direction: 'vertical',
                    slidesPerView: 1,
                    paginationClickable: true,
                    spaceBetween: 0,
                    mousewheelControl: true,
                    autoHeight: true
                }
            }
        }
        ,
        components: {
            swiper,
            swiperSlide
        }
    }
</script>

<style scoped>
    .ubuntu {
        background-color: #c34113;
    }

    .index {
        position: relative;
        height: 100%;
        width: 100%;
    }

    .h1 {
        position: relative;
        top: 40%;
        transform: translateY(-50%);
    }

    .right {
        position: absolute;
        right: 2%;
        top: 4%;
        z-index: 1;
    }
</style>
