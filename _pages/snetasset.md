---
layout: page-notitle
permalink: /snetasset/
title: snet-asset
pagination:
    enabled: true
    collection: "snet-asset"
    permalink: /page/:num/
    per_page: 15
    sort_field: 'order'
    sort_reverse: false
    trail:
    before: 1 # The number of links before the current page
    after: 3  # The number of links after the current page
    indexpage: 'snet-asset'
---
<header class="post-header center-text">
    <h1 class="post-title">ScenarioNet Demo</h1>
</header>
<div style="text-align: center;">
  <p>For faster loading times, we have compressed our videos.</p>
  <p>For optimal viewing experience, we recommend accessing this website on a computer using Chrome.</p>
</div>
<div id="tag-filter">
    <button class="filter-button" data-tag="all">All</button>
    {% for tag in site.data.tag %}
    <button class="filter-button" data-tag="{{ tag }}">{{ tag }}</button>
    {% endfor %}
</div>

<div class="infinite-scroll-gallery">
    <div class="image-gallery">
    <div class="sizer"></div>
    {% assign posts = paginator.posts%}
    {% for video in posts %}
    <div class="image" data-tag="{{ video.tag }}">
        <div class="video-container">
            <video loop muted autoplay playsinline  data-src="{{ video.src }}" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
        <div class="video-info" style="display: flex; justify-content: center; align-items: center; flex-direction: row; gap: 10px;">
            <div class="badge badge-tag">{{ video.tag }}</div>
            <div class="badge badge-id">{{ video.vid }}</div>
        </div>
    </div>
    {% endfor %}
    </div>
    {% if paginator.next_page %}
    <div class="pagination">
        <a href="{{ paginator.next_page_path }}" class="pagination__next">Next</a>
    </div>
    {% endif %}
</div>

<script>
function detectDeviceAndBrowser() {
    var userAgent = navigator.userAgent;

    var device = /Mobi|Android|iPhone|iPad|iPod/i.test(userAgent) ? 'Mobile' : 'Computer';
    
    var browser = 'Unknown';
    if (userAgent.indexOf('Chrome') > -1) {
        browser = 'Chrome';
    } else if (userAgent.indexOf('Safari') > -1) {
        browser = 'Safari';
    }
    
    return { device: device, browser: browser };
}

function shuffleArray(array) {
  for (let i = array.length - 1; i > 0; i--) {
    let j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
  return array;
}

document.addEventListener('DOMContentLoaded', function() {
    const POSTS_PER_PAGE = 15;
    var { device } = detectDeviceAndBrowser();
    var elem = document.querySelector('.image-gallery');
    var placeholderSrc = '../assets/scenarionet/transparent_video.mp4';
    console.log(navigator.userAgent);
    console.log(device);
    let options = {
      root: null,
      rootMargin: '0px',
      threshold: 0
    };
    
    let observer = new IntersectionObserver(onChange, options);
    function onChange(changes, observer) {
        changes.forEach(change => {
        let video = change.target;
        if (change.isIntersecting) {
            if (device === "Mobile" && video.getAttribute('src') == placeholderSrc) {
                video.src = video.getAttribute('data-src');
                video.load();
            }
            else if (!video.getAttribute('src') || !video.src) {
              video.src = video.getAttribute('data-src');
              video.load();
            }
        } 
        else {
            if (device === "Mobile") {
                video.pause();
                video.src = placeholderSrc;
                video.load();
                console.log("Unloading the video");
            }
        }
        });
    }

    var msnry = new Masonry( elem, {
    itemSelector: '.image', 
    columnWidth: '.sizer', 
    percentPosition: true
    });

    var imageElements = Array.from(document.querySelectorAll('.image'));
    shuffleArray(imageElements);
    imageElements.forEach(function(imageElement) {
        elem.appendChild(imageElement);
    });

    document.querySelectorAll('.image-gallery video').forEach(function(video) {
        initializeVideo(video);
        observer.observe(video);
    });

    var infScroll = new InfiniteScroll( elem, {
        path: 'a.pagination__next',
        append: '.image',
        history: false,
        scrollThreshold: 0,
        status: '.page-load-status',
        debug: true,
        outlayer: msnry,
    });
    infScroll.on('append', function(response, path, items) {
        shuffleArray(Array.from(items));
        items.forEach(function(item) {
          var video = item.querySelector('video');
          if (video) {
            initializeVideo(video);
            observer.observe(video);
          }
        });
        imagesLoaded( items, function() {
            msnry.layout();
        });
        var filterButtonActive = document.querySelector('.filter-button.active');
        var activeTag = filterButtonActive ? filterButtonActive.dataset.tag : 'all';
        filterVideos(activeTag);
        checkVisibleImages();
        msnry.layout();
    });


    function initializeVideo(video) {
        var rect = video.getBoundingClientRect();
        var isInViewport = rect.top <= window.innerHeight && rect.bottom >= 0;
        if (device === "Mobile") {
             if (isInViewport) {
                video.src = video.getAttribute('data-src');
            } else {
                video.src = placeholderSrc;
            }
            video.load();
        }
        video.onloadeddata = function() {
            console.log('Video data loaded.');
            msnry.layout();
        };
        
        video.onerror = function() {
            console.error('Error loading video:', video.src);
            console.log('Error code:', video.error.code);
            video.closest('.image').remove();
        };
        video.oncanplay = function() {
            video.play().catch(function(error) {
              console.error('Error attempting to play:', error);
            });
        };
    }

    window.addEventListener('resize', function() {
    msnry.layout();
    });

    var filterButtons = document.querySelectorAll('.filter-button');

    function filterVideos(tag) {
        console.log('Filtering videos for tag:', tag);
        var images = document.querySelectorAll('.image');
        images.forEach(function(image) {
            var video = image.querySelector('video');
            if (tag === 'all' || image.getAttribute('data-tag') === tag) {
                image.style.display = '';
                var rect = video.getBoundingClientRect();
                var isInViewport = rect.top <= window.innerHeight && rect.bottom >= 0;
                if (isInViewport) {
                    if (device === "Mobile" && video.getAttribute('src') == placeholderSrc) {
                        video.src = video.getAttribute('data-src');
                        video.load();
                    }
                    else if (!video.getAttribute('src') || !video.src) {
                        video.src = video.getAttribute('data-src');
                        video.load();
                    }
                }
            } else {
                image.style.display = 'none'
                if (video.getAttribute('src') && device === "Mobile") {
                    video.pause();
                    video.src = placeholderSrc;
                    video.load();
                }
            }
        });
        msnry.layout();
    }

    filterButtons.forEach(function(button) {
        button.addEventListener('click', function(event) {
        console.log('Tag filter changed:', event.target.dataset.tag);
        filterVideos(event.target.dataset.tag);
        infScroll.loadNextPage();
        msnry.layout();

        filterButtons.forEach(function(btn) {
            btn.classList.remove('active');
        });

        event.target.classList.add('active');
        });
    });

    function checkVisibleImages() {
        var images = document.querySelectorAll('.image:not([style*="display: none"])');
        if (images.length < POSTS_PER_PAGE) {
          infScroll.loadNextPage();
          msnry.layout();
        }
    }
});
</script>


