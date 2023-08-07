---
layout: page
permalink: "/success-stories/"
title: Succecc Stories


hero_second_image: "assets/img/slider/hero-second-image.webp"
hero_hedding_one: "Success Stories - Sanmark Solutions"
hero_background_color: rgba(16, 42, 84, 0.8)
opacity: 0.8
hero_hedding_one_font_size: 48px


animation1: hedding-animation
animation2: hero_second_image-animation

background_color: '#ffffff'
status: 'breadcrumb'
---

<div class="basic-blog-area gray-bg pt-100 pb-100 news-card-section">
    <div class="container" style="position: relative;">
        <div class="row justify-content-center">
            <div class="col-lg-8 col-12 d-flex justify-content-center">
                <div class="row justify-content-center news-active" id="paginated-list" data-current-page="1" aria-live="polite">
                    {% for stories in site.success_stories %}
                    <div
                        class="col-12 blog-wrapper mb-40 news-card  {% for category in stories.categoriesname %}{{ category }} {% endfor %} news-card-hidden">

                        <div class="blog-thumb news-card-image">
                            <a href="{{stories.url | relative_url}}">
                                <img src="{{stories.post_image | relative_url }}" width="450" height="338" alt="{{stories.title}}"
                                    class="img-fluid" />
                            </a>
                        </div>
                        <div class="meta-info d-flex justify-content-around">
                            <div class="d-flex align-items-center">
                                <span class="lnr lnr-calendar-full pr-3" style="color: #2e59c7 !important;"></span>
                                {{ stories.date | date_to_long_string }}
                            </div>
                            <div class="d-flex align-items-center">
                                <span class="lnr lnr-user pr-3" style="color: #2e59c7 !important;"></span>
                                {{ stories.author }}
                            </div>
                        </div>
                        <div class="blog-content">
                            <h2 class="blog-title">
                                <a href="{{stories.url | relative_url }}">{{stories.title}}</a>
                            </h2>
                        </div>
                        <div class="blog-detail">
                            <p>{{stories.excerpt | strip_html | truncatewords:"30"}}</p>
                        </div>
                        <div class="link-box">
                            <a href="{{stories.url| relative_url }}" style="color: #fff;"><button class="button-about grow_skew_forward"
                                    id="btn1">{{ stories.button }}</button></a>
                        </div>
                    </div>
                    {% endfor %}
                </div>
            </div>
            <div class="col-lg-4 col-12 pl-5 mt-3 news-menu">
                <div class="widget">
                    <h4 class="widget-title" style="font-size: 16px;">Categories</h4>
                    <div class="widget-link">
                        {% assign categories = "" | split: "," %}
                        {% for stories in site.success_stories %}
                        {% for category in stories.categories %}
                        {% unless categories contains category %}
                        {% assign categories = categories | push: category %}
                        {% endunless %}
                        {% endfor %}
                        {% endfor %}
                        <div class="row">
                            {% for catogary_name in categories %}
                            <div class="col-12 mt-2">
                                <style>
                                    .news-active {
                                        width: 100% !important;
                                        height: auto !important;
                                    }

                                    .news-active .blog-wrapper {
                                        width: 100%;
                                        position: relative !important;
                                        top: 0 !important;
                                        left: 0 !important;
                                        width: 90%;
                                    }

                                    .news-menu button {
                                        background: none;
                                        outline: none;
                                        border: none;
                                        color: #000;
                                        font-weight: bolder;
                                        font-size: 16px;
                                    }

                                    .news-menu button:hover {
                                        color: #445376;
                                    }
                                </style>
                                <button class="p-item" data-filter=".{{ catogary_name | remove: " " }}">
                                    {{ catogary_name | capitalize }}
                                </button>
                            </div>
                            {% endfor %}
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div>
            <nav class="page-navigation pagination ">
                <ul class="d-flex align-items-center justify-content-center">

                    <li class="page-item "><a class="page-link active" id="prev-button" title="Previous page"
                            aria-label="Previous page">Prev</a></li>

                    <li id="pagination-numbers" class="d-flex">
                    </li>

                    <li class="page-item "><a class="page-link" id="next-button" title="Next page"
                            aria-label="Next page">Next</a></li>
                </ul>
            </nav>
        </div>
    </div>
</div>

<script>
    document.addEventListener("DOMContentLoaded", function () {
        const paginatedList = document.getElementById("paginated-list");
        const prevButton = document.getElementById("prev-button");
        const nextButton = document.getElementById("next-button");
        const paginationNumbers = document.getElementById("pagination-numbers");

        const itemsPerPage = 10; // Number of items to show per page
        let currentPage = 1; // Current page number

        // Calculate the total number of pages
        const totalPages = Math.ceil(paginatedList.children.length / itemsPerPage);

        // Function to show the items for the current page
        function showPage(page) {
            const startIndex = (page - 1) * itemsPerPage;
            const endIndex = startIndex + itemsPerPage;

            for (let i = 0; i < paginatedList.children.length; i++) {
                const item = paginatedList.children[i];

                if (i >= startIndex && i < endIndex) {
                    item.style.display = "block";
                } else {
                    item.style.display = "none";
                }
            }
        }

        // Function to update the pagination numbers
        function updatePaginationNumbers() {
            paginationNumbers.innerHTML = "";

            for (let i = 1; i <= totalPages; i++) {
                const pageNumber = document.createElement("button");
                pageNumber.classList.add("pagination-number");
                pageNumber.textContent = i;

                if (i === currentPage) {
                    pageNumber.classList.add("active");
                }

                pageNumber.addEventListener("click", function () {
                    currentPage = i;
                    showPage(currentPage);
                    updatePaginationNumbers();
                });

                paginationNumbers.appendChild(pageNumber);
            }
        }

        // Function to go to the previous page
        function goToPreviousPage() {
            if (currentPage > 1) {
                currentPage--;
                showPage(currentPage);
                updatePaginationNumbers();
            }
        }

        // Function to go to the next page
        function goToNextPage() {
            if (currentPage < totalPages) {
                currentPage++;
                showPage(currentPage);
                updatePaginationNumbers();
            }
        }

        // Event listeners for the previous and next buttons
        prevButton.addEventListener("click", goToPreviousPage);
        nextButton.addEventListener("click", goToNextPage);

        // Show the initial page
        showPage(currentPage);
        updatePaginationNumbers();
    });

    $(document).ready(function () {
        $(".news-active").imagesLoaded(function () {
            var $grid = $(".news-active").isotope({
                itemSelector: ".news-card",
                percentPosition: true,
                masonry: {
                    // use outer width of grid-sizer for columnWidth
                    columnWidth: 1
                }
            });


            $(".news-menu").on("click", "button", function () {
                var filterValue = $(this).attr("data-filter");
                var elementhidden = $(".news-card-hidden");
                var elementsToShow = $(filterValue).filter(filterValue);
                var title = $(this).html();

                console.log(elementhidden);
                elementhidden.css("display","none")
                elementsToShow.css("opacity", 0).css("display", "block").animate({ opacity: 1 }, 500);
                event.preventDefault();
                $("#slider-heading").html(title + "- Sanmark Solution");
            });
        });

    });

</script>