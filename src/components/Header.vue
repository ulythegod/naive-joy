<template>
    <div class="header">
        <a href="/" class="logo">
            <span>НАИВНЫЙ ВОСТОРГ</span>
        </a>
        <i class="mobile-menu-button" v-on:click="open" style="display: none">
           <img src="../assets/list.png" data-mobile="../assets/list.png" data-desktop="../assets/list.png" alt="Кнопка меню">
        </i>
        <i class="mobile-menu-close-button js-mobile-menu-close-button" v-on:click="close" style="display: none">
           <img class="js-close-img" src="../assets/close.png" data-mobile="../assets/close.png" data-desktop="../assets/close.png" alt="Закрыть меню">
        </i>
        <ul class="top-nav">
            <li>
                <a href="#group">ГРУППА</a>
            </li>
            <li>
                <a href="#last-music">ПОСЛЕДНИЕ РЕЛИЗЫ</a>
            </li>
            <li>
                <a href="#music">МУЗ.ПЛОЩАДКИ</a>
            </li>
            <li>
                <a href="https://www.youtube.com/channel/UCU_lJ3QYq900oQqgTdnr6Hg">YOUTUBE</a>
            </li>
            <li class="social margin-left">
                <a href="https://www.instagram.com/bass.torg/" target="_blank">
                    <i class="logo-menu-desktop logo-instagram"></i>
                </a>
            </li>
            <li class="social">
                <a href="https://vk.com/basstorg" target="_blank">
                    <i class="logo-menu-desktop logo-vk"></i>
                </a>
            </li>
            <li class="social">
                <a href="https://twitter.com/basstorg" target="_blank">
                    <i class="logo-menu-desktop logo-twitter"></i>
                </a>
            </li>
        </ul>
        <ul class="top-nav-mobile js-top-nav-mobile" style="display: none">
            <li>
                <a v-on:click="close" href="#group">ГРУППА</a>
            </li>
            <li>
                <a v-on:click="close" href="#last-music">ПОСЛЕДНИЕ РЕЛИЗЫ</a>
            </li>
            <li>
                <a v-on:click="close" href="#music">МУЗ.ПЛОЩАДКИ</a>
            </li>
            <li>
                <a v-on:click="close" href="https://www.youtube.com/channel/UCU_lJ3QYq900oQqgTdnr6Hg">YOUTUBE</a>
            </li>
            <li class="social margin-left">
                <a v-on:click="close" href="https://www.instagram.com/bass.torg/" target="_blank">
                    <i class="logo-menu-mobile logo-instagram-w"></i>
                </a>
            </li>
            <li class="social">
                <a v-on:click="close" href="https://vk.com/basstorg" target="_blank">
                    <i class="logo-menu-mobile logo-vk-w"></i>
                </a>
            </li>
            <li class="social">
                <a v-on:click="close" href="https://twitter.com/basstorg" target="_blank">
                    <i class="logo-menu-mobile logo-twitter-w"></i>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    methods: {
        open: function () {
            document.querySelector(".js-top-nav-mobile").style.display = "flex";
            document.querySelector(".js-close-img").style.display = "block";
            document.querySelector(".js-mobile-menu-close-button").style.display = "inline-block";
        },
        close: function() {
            document.querySelector(".js-top-nav-mobile").style.display = "none";
            document.querySelector(".js-close-img").style.display = "none";
            document.querySelector(".js-mobile-menu-close-button").style.display = "none";
        }
    }
}
</script>

<style>
.header {
    background: white;
    position: fixed;
    z-index: 100;
    top: 0;
    left: 0;
    margin: 0 auto;
    display: flex;
    justify-content: flex-end;
    width: 100%;
    padding: 0 30px;
    height: 70px;
}

.header .logo {
    margin-right: auto;
    align-self: center;
}

.header a {
    text-decoration: none;
    transition: color 0.5s ease, border 0.5s ease, background 0.5s ease;
}

.header a:hover {
    opacity: 0.8;
}

.header .logo span {
    height: 20px;
    width: auto;
    color: black;
    font-size: 30px;
    text-transform: uppercase;
}

.top-nav {
    display: flex;
}

.header ul li {
    display: inline-block;
    position: relative;
}

.header ul li a {
    color: #000000;
    height: 70px;
    line-height: 70px;
    display: block;
    font-size: 14px;
    padding: 0px 2px;
    position: relative;
    text-transform: uppercase;
    transition: opacity 0.5s ease;
    opacity: 1;
    letter-spacing: 0.5em;
    text-indent: 0.5em;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased !important;
    -moz-font-smoothing: antialiased !important;
    text-rendering: optimizelegibility !important;
    vertical-align: middle;
}

.header ul li a:hover {
    opacity: 0.8;
}

.header ul li.social a {
    padding: 0px;
    font-size: 19px;
    letter-spacing: 0px;
    text-indent: 0px;
    margin-right: 40px;
}

.header ul li.social a:hover {
    opacity: 0.7;
}

.header ul li.margin-left {
    margin-left: 20px;
}

.logo-menu-desktop:before {
    width: 18px; 
    height: 18px;
    background-size: 18px 18px;
    display: inline-block;
    content:"";
}

.logo-twitter:before {
    background-image: url("../assets/twitter.png");
}

.logo-instagram:before {
    background-image: url("../assets/instagram.png");
}

.logo-vk:before {
    background-image: url("../assets/vk.png");
}

@media (max-device-width: 1246px) {
    .header ul li.margin-left {
        margin-left: 5px;
    }

    .header ul li.social a {
        margin-right: 32px;
    }

    .header .logo span {
        font-size: 25px;
    }
}

@media (max-device-width: 1157px) {
    .top-nav {
        display: none;
    }
    
    .mobile-menu-button {
        display: inline-block !important;
        position: absolute;
        right: 35px;
        top: 0px;
        font-size: 21px;
        line-height: 60px;
        cursor: pointer;
    }

    .mobile-menu-button img {
        position: relative;
        width: 24px;
        height: 19px;
        right: inherit;
    }

    .top-nav-mobile {
        height: 100vh;
        display: flex;
        position: absolute;
        top: 0px;
        background: #000000;
        width: 100%;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        align-content: center;
        font-size: 0px;
    }

    .top-nav-mobile li {
        display: block;
        width: 100%;
        text-align: center;
    }

    .top-nav-mobile li a {
        color: white !important;
    }

    .top-nav-mobile li.social {
        width: auto;
        margin-left: 40px !important;
        text-align: center;
    }

    .logo-menu-mobile:before {
        width: 18px; 
        height: 18px;
        background-size: 18px 18px;
        display: inline-block;
        content:"";
    }

    .logo-twitter-w:before {
        background-image: url("../assets/twitter_w.png");
    }

    .logo-instagram-w:before {
        background-image: url("../assets/instagram_w.png");
    }

    .logo-vk-w:before {
        background-image: url("../assets/vk_w.png");
    }

    .mobile-menu-close-button {
        display: inline-block !important;
        position: absolute;
        right: 79px;
        top: 38px;
        font-size: 36px;
        line-height: 60px;
        cursor: pointer;
        color: #ffffff;
        z-index: 100;
    }

    .mobile-menu-close-button img {
        position: relative;
        width: 15px;
        height: 15px;
        display: none;
    }
}
</style>