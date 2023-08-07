---
layout: default
permalink: /contact/
title: Contact Sanmark for Your Software Development Needs
description: "Contact Sanmark for Custom Software Development, Dedicated Engineers (Staff Augmentation), and Software Teams for Hire for Australia for Affordable Prices."


hero_background_image: "assets/img/slider/testimonials_hero_background_image.webp"
hero_second_image: "assets/img/slider/hero-second-image.webp"
hero_hedding_one: Contact Sanmark for Your Software Development Needs
hero_hedding_one_font_size: 38px
hero_background_color: rgba(16, 42, 84, 0.8)
opacity: 0.8

animation1: hedding-animation
animation2: hero_second_image-animation

background_color: '#E7EDF8'
status: 'breadcrumb'

test: "assets/img/contact/01.webp"

location_image: "/assets/img/contact/location.webp"

office_location_bg_image: "assets/img/contact/14.webp"
---
{% include header.html %}

<main>
<style>
    @media screen and (max-width: 991px) {
 

  .slider-area{
    height: 180px;
  }


}
</style>
    {% include slider.html %}
    <div class="slider-bottom-svg" style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
    </div>
    {% include contact_card.html %}
    {% include contact_location.html %}
    {% include office_locations.html %}
    {% include testimonials.html %}

    
    <script>

    $(document).ready(function () {
        var owl = $('.owl-carousel');
        owl.owlCarousel();
        $('.customNextBtn').click(function () {
            owl.trigger('next.owl.carousel');
        })
        $('.customPrevBtn').click(function () {
            owl.trigger('prev.owl.carousel', [300]);
        })
    });

    $(document).ready(function() {
 
 $("#owl-demo").owlCarousel({

     autoPlay: 3000, //Set AutoPlay to 3 seconds

     items : 4,
     itemsDesktop : [1199,3],
     itemsDesktopSmall : [979,3]

 });

});
</script>
</main>


