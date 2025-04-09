---
layout: research
permalink: /ucla_ucb_workshop/
title: UCLA-UCB Joint Workshop
page_title: 
description: 
nav: false
nav_order: 1
---




<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>


<style>
.title {
    color: #414446;
    clear: both;
    text-align: center;
}

.title-main {
    font-size: 20pt; /* Adjust main title size */
}

.title-sub {
    font-size: 18pt; /* Adjust subtitle size */
}

.time, .location {
    font-size: 12pt; /* Adjust time and location font size */
}

.logo {
    width: 100%;
    padding: 2px 2px 2px 2px;
    margin: 0px 0px 1px 0px;
    object-fit: contain;
}

.caption {
    padding: 3px 0px 3px 0px;
    margin: 0px 0px 3px 0px;
    text-align: center;
    font-size: 14pt;
}
.caption span {
    font-size: 10pt;
}
.caption a:hover {text-decoration:none;}

.carousel-item {
    text-align: center;
}
.carousel-caption {
    background: rgba(230, 230, 230, 0.9);
}

.thumbnail {
    padding: 2px 2px 2px 2px;
    margin: 0px 0px 1px 0px;
}

.thumbnail img {
    height: 200px;
    object-fit: scale-down;
    width: 100%;
}
@media (min-width: 576px) {
    .thumbnail img {
        object-fit: cover;
    }
    .thumbnail img.top-left {
        object-position: 0px 0px;
    }
}
 

.thumbnail ul {
    display: block;
    list-style-type: none;
    margin: 0px;
    padding: 5px;
    text-align: center;
}
@media (hover: hover) {
    .thumbnail div {
        position: relative;
        overflow: hidden;
    }
    .thumbnail ul {
        background: rgba(200, 200, 200, 0.7);
        position: absolute;
        bottom: -100%;
        left: 0px;
        right: 0px;
        transition: bottom 0.2s ease-in-out;
    }
    .thumbnail:hover ul {
        bottom: 0px;
    }
}


</style>

<div class="title">
                <h2 class="title-main">1st UCLA-UCB Joint Workshop:</h2>
                <h2 class="title-sub">Towards Next Generation of Open-Source Simulator for Embodied AI and Autonomous Driving</h2>
                <h5 class="time">Time: 9:50 am to 1:00 pm, Feb 10, 2025</h5>
                <h5 class="location">Location: 8034 Berkeley Way West</h5>
</div>

<div id="carouselExampleDark" class="carousel carousel-dark slide" data-bs-ride="carousel">
                  <div class="carousel-indicators">
                    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
                  </div>
                  <div class="carousel-inner">
                    <div class="carousel-item active" data-bs-interval="15000">
                      <video autoplay muted loop width="100%">
                        <source src="/assets/img/ucla_ucb_workshop/carousel/metaurban short.mp4" type="video/mp4">
                      </video>
                      <div class="carousel-caption d-none d-md-block">
                        <h5>MetaUrban: An Embodied AI Simulation Platform for Urban Micromobility</h5>
                        <p>ICLR 2025</p>
                      </div>
                    </div>
                    <div class="carousel-item" data-bs-interval="15000">
                      <video autoplay muted loop width="100%">
                        <source src="/assets/img/ucla_ucb_workshop/carousel/metadrive_teaser.mp4" type="video/mp4">
                      </video>
                      <div class="carousel-caption d-none d-md-block">
                        <h5>MetaDrive: AI Research for Generalizable and Interpretable Machine Autonomy</h5>
                        <p>TPAMI 2021</p>
                      </div>
                    </div>
                  </div>
                  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                  </button>
                  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                  </button>
                </div>
<!-- JavaScript to Control Video Playback on Slide Change -->
<script>
    // Select carousel element and all videos
    const carousel = document.getElementById('carouselExampleDark');
    const videos = document.querySelectorAll('.carousel-video');

    // Add event listener to handle slide change
    carousel.addEventListener('slide.bs.carousel', function (event) {
        // Pause all videos
        videos.forEach(video => video.pause());

        // Find the newly active slide and play the video inside it
        const activeSlide = event.relatedTarget;
        const video = activeSlide.querySelector('video');
        if (video) {
            video.play();
        }
    });
</script>


---

## 📅 Schedule
The workshop will take place on **Monday, Feb 10, 2025**, at **8034 Berkeley Way West** (PST).  

<iframe 
    src="https://docs.google.com/spreadsheets/d/e/2PACX-1vT4Rxz3976F0y7fb3rvmvNH62oICvYBmKMuO1i5n083gjujX1dTCC-9j1ACbjJB5xs6bB-Xdopde2u1/pubhtml?gid=1254621366&single=true&chrome=false&widget=false&headers=false"
    width="100%" height="500">
</iframe>

---

## 🎤 Speakers

 
<div class="row">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/Jitendra_Malik.jpg" alt="Jitendra Malik">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~malik/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Jitendra Malik<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/angjoo_photo.jpg" alt="Angjoo Kanazawa">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~kanazawa/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Angjoo Kanazawa<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/Trevor_Darrell.jpeg" alt="Trevor Darrell">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~trevor/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Trevor Darrell<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/weizhan.webp" alt="Wei Zhan">
                <ul class="social">
                    <a href="https://zhanwei.site/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Wei Zhan<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
</div>

<div class="row">
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/spotlight/wayne.png" alt="Wayne Wu">
                            <ul class="social">
                                <a href="https://wywu.github.io/">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            Wayne Wu<br><span>University of California, Los Angeles</span>
                        </div>
                    </div>
                </div>
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/spotlight/honglin.webp" alt="Honglin He">
                            <ul class="social">
                                <a href="https://dhlinv.github.io/">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            Honglin He<br><span>University of California, Los Angeles</span>
                        </div>
                    </div>
                </div>
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/spotlight/zhizheng.png" alt="Zhizheng Liu">
                            <ul class="social">
                                <a href="https://scholar.google.com/citations?user=Asc7j9oAAAAJ&hl=en">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            Zhizheng Liu<br><span>University of California, Los Angeles</span>
                        </div>
                    </div>
                </div>
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/spotlight/david.jpg" alt="David McAllister">
                            <ul class="social">
                                <a href="https://mcallisterdavid.com/">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            David McAllister<br><span>University of California, Berkeley</span>
                        </div>
                    </div>
                </div>
            </div>

<div class="row">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/hongsuk.png" alt="Hongsuk Choi">
                <ul class="social">
                    <a href="https://hongsukchoi.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Hongsuk Choi<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/QianqianWang.jpg" alt="Qianqian Wang">
                <ul class="social">
                    <a href="https://qianqianwang68.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Qianqian Wang<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/yifei.png" alt="Yifei Zhang">
                <ul class="social">
                    <a href="https://forrest-110.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Yifei Zhang<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/grace.jpeg" alt="Grace Luo">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~graceluo/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Grace Luo<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
</div>

<div class="row">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/junyi.jpg" alt="Junyi Zhang">
                <ul class="social">
                    <a href="https://www.junyi42.com/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Junyi Zhang<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/sicheng.webp" alt="Sicheng Mo">
                <ul class="social">
                    <a href="https://sichengmo.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Sicheng Mo<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/spotlight/seth.png" alt="Seth Zhao">
                <ul class="social">
                    <a href="https://sethzhao506.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Seth Zhao<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
</div>
               

---

## 🏆 Organizers
### Principal Investigators:
<div class="row">
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/organizers/bolei.jpg" alt="Bolei Zhou">
                <ul class="social">
                    <a href="https://boleizhou.github.io/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Bolei Zhou<br><span>University of California, Los Angeles</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/angjoo_photo.jpg" alt="Angjoo Kanazawa">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~kanazawa/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Angjoo Kanazawa<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>
    <div class="col-xs-6 col-md-3">
        <div class="thumbnail">
            <div>
                <img src="/assets/img/ucla_ucb_workshop/speakers/Trevor_Darrell.jpeg" alt="Trevor Darrell">
                <ul class="social">
                    <a href="https://people.eecs.berkeley.edu/~trevor/">
                        <li class="icon"><i class="fa fa-home"></i></li>
                    </a>
                </ul>
            </div>
            <div class="caption">
                Trevor Darrell<br><span>University of California, Berkeley</span>
            </div>
        </div>
    </div>

</div>

### Workshop Coordinators:
<div class="row">
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/organizers/wayne.png" alt="Wayne Wu">
                            <ul class="social">
                                <a href="https://wywu.github.io/">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            Wayne Wu<br><span>University of California, Los Angeles</span>
                        </div>
                    </div>
                </div>
                <div class="col-xs-6 col-md-3">
                    <div class="thumbnail">
                        <div>
                            <img src="/assets/img/ucla_ucb_workshop/speakers/weizhan.webp" alt="Wei Zhan">
                            <ul class="social">
                                <a href="https://zhanwei.site/">
                                    <li class="icon"><i class="fa fa-home"></i></li>
                                </a>
                            </ul>
                        </div>
                        <div class="caption">
                            Wei Zhan<br><span>University of California, Berkeley</span>
                        </div>
                    </div>
                </div>
            </div>

---

## 🎗️ Sponsor
<div class="row justify-content-center align-items-center">
    <div class="col-xs-3 col-md-3 col-img">
        <img src="/assets/img/ucla_ucb_workshop/logos/nsf.png" alt="NSF" class="logo">
    </div>
    <div class="col-xs-4 col-md-4 col-img">
        The workshop is supported by <b>NSF CCRI grants 2235012 and 2235013</b>.
    </div> 
</div>
