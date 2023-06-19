---
layout: page-notitle
permalink: /snetasset/
title: test
pagination:
    enabled: true
    collection: "images"
    permalink: /page/:num/
    per_page: 12
    sort_field: date
    sort_reverse: true
    trail:
        before: 1 # The number of links before the current page
        after: 3  # The number of links after the current page
    indexpage: 'image'
---

<div class="infinite-scroll-gallery">
    <div class="image-gallery">
        {% for image in paginator.posts %}
        <div class="image">
            <img src="{{ image.src }}" alt="{{ image.src }}">
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
document.addEventListener('DOMContentLoaded', function() {
  var elem = document.querySelector('.image-gallery');
  var msnry = new Masonry( elem, {
    itemSelector: '.image', 
    columnWidth: '.image', 
    percentPosition: true
  });

  var infScroll = new InfiniteScroll( elem, {
    path: 'a.pagination__next',
    append: '.image',
    history: false,
    scrollThreshold: 300,
    status: '.page-load-status',
    debug: true,
    outlayer: msnry,  // use Masonry as the layout view
  });

  infScroll.on('append', function(response, path, items) {
    setTimeout(function() {
        items.forEach(function(item) {
            // layout Masonry after each image loads
            imagesLoaded(item.element, function() {
                msnry.appended(item.element);
            });
        });
    }, 100);
  });
});


</script>













