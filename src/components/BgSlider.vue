<template>
    <div class="bg-slider">
        <swiper
            :slides-per-view="1"
            :space-between="50"
            :loop="true"
            :speed="1000"
            :effect="'fade'"
            :autoplay="{
                delay: 4000,
                disableOnInteraction: false,
            }"
            :allowTouchMove="false"
            :modules="modules"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
        >
            <swiper-slide>
                <img src="@/assets/img/slide-1.jpg" alt="">
            </swiper-slide>
            <swiper-slide>
                <img src="@/assets/img/slide-2.jpg" alt="">
            </swiper-slide>
            <swiper-slide>
                <img src="@/assets/img/slide-3.jpg" alt="">
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/effect-fade';

import {EffectFade, Autoplay } from 'swiper/modules';

export default {
    name: "BgSlider",
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const onSwiper = (swiper) => {};
        const onSlideChange = () => {};
        return {
            onSwiper,
            onSlideChange,
            modules: [EffectFade, Autoplay],
        };
    },
}
</script>

<style>

</style>