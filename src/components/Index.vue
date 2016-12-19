<template>
    <div class="index">
        <swiper :options="swiperOption" style="height: 100%">
            <div id='right'>
                <button type="button" class="btn btn-danger ubuntu" v-on:click="go_url">
                    {{ displayVersion() }}
                </button>
            </div>
            <swiper-slide v-for="title in titles" v-bind:style='title.theme'>
                <h1 class="h1 text-center">{{ title.main_title }}
                    <small v-bind:style='title.theme_small'>{{ title.sub_title }}</small>
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
            displayVersion: function () {
                if (this.isRolling()) {
                    return '实时推进';
                }
                else {
                    return '稳定版';
                }
            },
            go_url: function () {
                if (this.isRolling()) {
                    window.location.href = 'https://rolling.muyu.party';
                }
                else {
                    window.location.href = 'https://www.muyu.party';
                }
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
                        main_title: 'Coding',
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
                        sub_title: '星际议会',
                        theme: {
                            color: 'white',
                            backgroundColor: 'rgb(0, 162, 202)',
                        },
                        theme_small: {
                            color: '#ccc',
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

    #right {
        position: absolute;
        right: 2%;
        top: 4%;
        z-index: 1;
    }
</style>
