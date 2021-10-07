<template>
    <div class="wrapper">
        <div class="modules">
            <div id="group" class="module">
                <a href="https://vk.com/topic-195571734_47998245" target="_blank">
                    <img src="../assets/band.jpg" data-mobile="../assets/band.jpg" data-desktop="../assets/band.jpg" alt="Наивный восторг">
                </a>
            </div>
            <div id="last-music" class="module">
                <p class="block-title">Последние музыкальные новинки</p>
                <ul class="music-module">                    
                    <li>
                        <p>Дом под снос (cover)</p>
                        <a href="https://youtu.be/WG4cnLRv-z8" target="_blank">
                            <img src="../assets/dom.jpg" data-mobile="../assets/dom.jpg" data-desktop="../assets/dom.jpg" alt="Дом под снос кавер">
                        </a>
                    </li>
                    <li>
                        <p>Тупик</p>
                        <a href="https://youtu.be/30BI9nQQFt0" target="_blank">
                            <img src="../assets/typik.jpg" data-mobile="../assets/typik.jpg" data-desktop="../assets/typik.jpg" alt="Тупик">
                        </a>
                    </li>
                    <li>
                        <p>Я сделаю все</p>
                        <a href="https://youtu.be/0qitTWIR120" target="_blank">
                           <img src="../assets/sdelay.jpg" data-mobile="../assets/sdelay.jpg" data-desktop="../assets/sdelay.jpg" alt="Я сделаю все">
                        </a>
                    </li>
                </ul>
            </div>
            <div id="music" class="module">
                <p class="block-title">Наивный восторг на музыкальных площадках</p>
                <ul class="social-network-module">                    
                    <li class="social">
                        <a href="https://open.spotify.com/artist/2Z0OoPaLGem5JpLkKkxe2b?si=-naJ5JFiQ3WGp63zQKzU6Q&dl_branch=1" target="_blank">
                            <i class="logo-spotify-module"></i>
                        </a>
                    </li>
                    <li class="social">
                        <a href="https://music.apple.com/ru/artist/%D0%BD%D0%B0%D0%B8%D0%B2%D0%BD%D1%8B%D0%B9-%D0%B2%D0%BE%D1%81%D1%82%D0%BE%D1%80%D0%B3/1552646498" target="_blank">
                            <i class="logo-apple-module"></i>
                        </a>
                    </li>
                    <li class="social">
                        <a href="https://music.yandex.ru/artist/10862089" target="_blank">
                            <i class="logo-yandex-module"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style>
.wrapper {
    margin-top: 70px;
}

.modules .module {
    position: relative;
    cursor: pointer;
    font-size: 0px;
}

.modules .module img {
    width: 100%;
    height: auto;
}

.social-network-module {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin-top: 50px;   
}

.social-network-module ul li.social a {
    padding: 0px;
    font-size: 19px;
    letter-spacing: 0px;
    text-indent: 0px;
    margin-right: 40px;
}

.social-network-module ul li.social a:hover {
    opacity: 0.7;
}

.social-network-module ul li {
    margin-left: 10px;
    margin-right: 10px;
}

.logo-yandex-module:before {
    background-image: url("../assets/yandex.png");
    width: 300px; 
    height: 300px;
    background-size: 300px 300px;
    display: inline-block;
    content:"";
}

.logo-spotify-module:before {
    background-image: url("../assets/spotify.png");
    width: 300px; 
    height: 300px;
    background-size: 300px 300px;
    display: inline-block;
    content:"";
}

.logo-apple-module:before {
    background-image: url("../assets/music.png");
    width: 300px; 
    height: 300px;
    background-size: 300px 300px;
    display: inline-block;
    content:"";
}

.block-title {
    padding: 0px;
    font-size: 40px;
    letter-spacing: 0px;
    text-indent: 0px;
    text-align: center;
}

.music-module {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin-top: 50px;
}

.music-module p {
    font-size: 20px;
    text-align: center;
}

.music-module img {
    height: 400px !important;
    width: 400px !important;
}

.music-module img:hover {
    opacity: .8;
}

@media (max-device-width: 1246px) {
    .music-module img {
        height: 300px !important;
        width: 300px !important;
    }
}

@media (max-device-width: 1024px) {
    .music-module {
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }

    .social-network-module {
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }
    
    .social-network-module li {
        padding-top: 5px;
        padding-bottom: 5px;
    }
}

@media (max-device-width: 420px) {
    .music-module img {
        height: 250px !important;
        width: 250px !important;
    }

    .logo-yandex-module:before {
        width: 250px; 
        height: 250px;
        background-size: 250px 250px;
    }

    .logo-spotify-module:before {
        width: 250px; 
        height: 250px;
        background-size: 250px 250px;
    }

    .logo-apple-module:before {
        width: 250px; 
        height: 250px;
        background-size: 250px 250px;
    }
}

@media (max-device-width: 340px) {
    .music-module img {
        height: 200px !important;
        width: 200px !important;
    }

    .logo-yandex-module:before {
        width: 200px; 
        height: 200px;
        background-size: 200px 200px;
    }

    .logo-spotify-module:before {
        width: 200px; 
        height: 200px;
        background-size: 200px 200px;
    }

    .logo-apple-module:before {
        width: 200px; 
        height: 200px;
        background-size: 200px 200px;
    }

    .header .logo span {
        font-size: 20px;
    }

    .block-title {
        font-size: 20px;
    }

    .music-module {
        margin-top: 10px;
    }

    .social-network-module {
        margin-top: 10px;
    }
}
</style>