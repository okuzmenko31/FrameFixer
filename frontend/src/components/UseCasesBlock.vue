<template>
    <div class="wrapper-cont-cont">
        <p class="brand_text no-margin">Use cases</p>
        <p class="fs--50 header_text fw--900 align_center_text no-top">Frame Fixer</p>
        <div class="wrapper">
            <div class="box1 box">
                <p class="fs--20">Print</p>
                <p class="fs--15">Improve Images for Web Design, Print, Product Discovery, and Recommendations.</p>
            </div>
            <div class="box2 box">
                <p class="fs--20">E-commerce</p>
                <p class="fs--15">Effortlessly Enhance Website Sales with Image Noise Reduction in Minutes.</p>
            </div>
            <div class="box3 box">
                <p class="fs--20">Graphic Design</p>
                <p class="fs--15">Increase Images, Assets, Textures, Photos, and Graphics Instantly.</p>
            </div>
            <div class="box4 box">
                <p class="fs--20">Real Estate</p>
                <p class="fs--15">Perfect Real Estate Marketing Images: Enhance Colors and Photo Resolution.</p>
            </div>
            <div class="box5 box">
                <p class="fs--20">Digital painting</p>
                <p class="fs--15">Automatically Enhance Luxurious Art Digital Paintings: Increase Resolution and Add Details for Wallpaper with AI.</p>
            </div>
        </div>
        <div class="swiper-container">
            <swiper
                :modules="modules"
                :slides-per-view="1"
                :space-between="50"
                navigation
                :allowTouchMove="false"
                :pagination="{ clickable: true }"
                @swiper="onSwiper"
                @slideChange="onSlideChange"
            >
                <swiper-slide>
                    <div class="box1 box">
                        <p class="fs--20">Print</p>
                        <p class="fs--15">Improve Images for Web Design, Print, Product Discovery, and Recommendations.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="box2 box">
                        <p class="fs--20">E-commerce</p>
                        <p class="fs--15">Effortlessly Enhance Website Sales with Image Noise Reduction in Minutes.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="box3 box">
                        <p class="fs--20">Graphic Design</p>
                        <p class="fs--15">Increase Images, Assets, Textures, Photos, and Graphics Instantly.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="box4 box">
                        <p class="fs--20">Real Estate</p>
                        <p class="fs--15">Perfect Real Estate Marketing Images: Enhance Colors and Photo Resolution.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="box5 box">
                        <p class="fs--20">Digital painting</p>
                        <p class="fs--15">Automatically Enhance Luxurious Art Digital Paintings: Increase Resolution and Add Details for Wallpaper with AI.</p>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<script>
    import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import { A11y, Navigation, Pagination } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';

    export default {
        components: {
            Swiper,
            SwiperSlide,
        },
        setup() {
            return {
                modules: [Navigation, Pagination, A11y],
            };
        },
    };
</script>

<style>
.wrapper-cont-cont {
    display: flex;
    width: 100%;
    z-index: 1;
    min-width: 0;
    flex-direction: column;
    align-items: center;
}

.wrapper {
    display: grid;
    width: 80%;
    margin: 0 auto;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 100px;
    gap: 20px;
    z-index: 1;
    min-width: 0;
}

.box1 {
    grid-column-start: 2;
    grid-column-end: 4;
    grid-row-start: 1;
    grid-row-end: 3;
    background: linear-gradient( rgb(102, 0, 255, 0.5), rgba(177, 27, 27, 0.5) ), url('https://d2ahk8dombjwkf.cloudfront.net/website_images/poster.webp');
    background-repeat: no-repeat;
    background-size: cover;
}

.box2 {
    grid-column-start: 1;
    grid-row-start: 1;
    grid-row-end: 8;
    background: linear-gradient( rgba(177, 27, 27, 0.5), rgb(102, 0, 255, 0.5) ), url('https://d2ahk8dombjwkf.cloudfront.net/website_images/ecommerce.webp');
    background-repeat: no-repeat;
    background-size: cover;
}

.box3 {
    grid-column-start: 2;
    grid-row-start: 3;
    grid-row-end: 8;
    background: linear-gradient( rgb(102, 0, 255, 0.5), rgba(177, 27, 27, 0.5) ), url('https://d2ahk8dombjwkf.cloudfront.net/website_images/graphicdesignpng.webp');
    background-repeat: no-repeat;
    background-size: cover;
}

.box4 {
    grid-column-start: 3;
    grid-row-start: 3;
    grid-row-end: 10;
    background: linear-gradient( rgba(177, 27, 27, 0.5), rgb(102, 0, 255, 0.5) ), url('https://d2ahk8dombjwkf.cloudfront.net/website_images/realestate.webp');
    background-repeat: no-repeat;
    background-size: cover;
}

.box5 {
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 8;
    grid-row-end: 10;
    background: linear-gradient( rgb(102, 0, 255, 0.5), rgba(177, 27, 27, 0.5) ), url('https://d2ahk8dombjwkf.cloudfront.net/website_images/painting.webp');
    background-repeat: no-repeat;
    background-size: cover;
}

.box {
    background-color: #fff;
    color: #fff;
    border-radius: 20px;
    padding: 50px;
    box-sizing: border-box;
}

.swiper-container{
    display: none;
    min-height: 0;
    min-width: 0;
    max-width: 100vw; 
    width: 100%;
    overflow: hidden;
}

.swiper-slide{
    width: auto;
    flex-shrink: 0;
    display: block;
}

.swiper-wrapper{
    display: flex;
}

.swiper-pagination-bullet {
    background-color: rgba(0, 0, 0, 0.5);
    opacity: 1;
}

.swiper-pagination-bullet-active {
    opacity: 1;
    background: var(--swiper-pagination-color, var(--swiper-theme-color));
    background-color: #d091fa;
}

.swiper-button-next,
.swiper-button-prev {
    top: 50%;
    color: #d091fa !important;
    fill: black !important;
    stroke: black !important;
}

@media (min-width: 768px) and (max-width: 991px) {
    .wrapper {
        display: none;
    }

    .swiper-container {
        display: flex;
        max-width: 90vw; 
    }

    .box {
        height: 100%;
    }
}

@media (min-width: 651px) and (max-width: 767px) {
    .wrapper {
        display: none;
    }

    .swiper-container {
        display: flex;
        max-width: 90vw; 
    }

    .box {
        height: 100%;
    }
}

@media (min-width: 481px) and (max-width: 650px) {
    .wrapper {
        display: none;
    }

    .swiper-container {
        display: flex;
        max-width: 90vw; 
    }

    .box {
        height: 100%;
    }
}

@media (max-width: 480px) {
    .wrapper {
        display: none;
    }
    
    .swiper-container {
        display: flex;
        max-width: 90vw; 
    }
    
    .box {
        height: 100%;
    }
}
</style>