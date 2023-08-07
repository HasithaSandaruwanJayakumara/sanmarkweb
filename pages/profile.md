---
layout: default
permalink: /profile/
title: Profile
description: "Sanmark Solutions is a Software Development Company providing Custom Software Development, Staff Augmentation, Ecommerce, and Web Development Services."

hero_background_image: "assets/img/slider/testimonials_hero_background_image.webp"
hero_second_image: "assets/img/slider/testimonials_second_image.webp"
hero_hedding_one: Profile - Sanmark Solutions PVT LTD
hero_hedding_one_font_size: 38px
hero_background_color: rgba(16, 42, 84, 0.8)
opacity: 0.8

animation1: hedding-animation
animation2: hero_second_image-animation

background_color: '#E7EDF8'
status: 'breadcrumb' 

client_title: NOTABLE CLIENTS
client_hedding: Happy Clients
section_name: client_profile

contact:
    background: "#E7EDF8"
    form_description_animation: fade-in
    form_description_animation_delay: 150
    form_animation: fade-in
    form_animation_delay: 300

testimonial:
    background_color: '#ffffff'

technology:
  class_one: technologies-active
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
    <div style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
    </div>
    {% include profile_description.html %}
    {% include testimonials.html %}
    {% include profile_projects.html %}
    {% include technologies_carousel.html links=site.data.technologies  class_one=page.technology.class_one %}
    {% include profile_clients.html links=site.data.profile_clients title=page.client_title hedding=page.client_hedding name=page.section_name%}
    {% include contact.html %}

<script>
    $(document).ready(function () {
        var owl1 = $('#carouselOne .owl-carousel'); // Target the first carousel
        owl1.owlCarousel();
        $('#carouselOne .customNextBtn').click(function () { // Target the next button of the first carousel
            owl1.trigger('next.owl.carousel');
        });
        $('#carouselOne .customPrevBtn').click(function () { // Target the previous button of the first carousel
            owl1.trigger('prev.owl.carousel', [300]);
        });
    });

    $(document).ready(function () {
        var owl2 = $('#carouselTwo .owl-carousel'); // Target the second carousel
        owl2.owlCarousel();
        $('#carouselTwo .customNextBtn').click(function () { // Target the next button of the second carousel
            owl2.trigger('next.owl.carousel');
        });
        $('#carouselTwo .customPrevBtn').click(function () { // Target the previous button of the second carousel
            owl2.trigger('prev.owl.carousel', [300]);
        });
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
