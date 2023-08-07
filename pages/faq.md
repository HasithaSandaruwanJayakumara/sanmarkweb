---
layout: default  
permalink: "/faq/"


title: FAQ

hero_background_image: "assets/img/slider/testimonials_hero_background_image.webp"
hero_hedding_one: Most Common Questions About Our Service
hero_hedding_one_font_size: 48px
hero_background_color: rgba(16, 42, 84, 0.8)
opacity: 0.8
status: 'breadcrumb'
background_color: "#E7EDF8"

animation1: hedding-animation
animation2: hero_second_image-animation

faq_quections: true

faq:
  status: "one-circle_faq_main"
  padding_bottom: pb-60
  
---
{% include header.html %}
{% include slider.html %}
<div style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
</div>
{% include intro_section.html link=site.data.colapse_data.colapseData_FAQ status=page.faq.status %}
{% include testimonials.html %}
{% include contact.html %}
<style>
    @media screen and (max-width: 991px) {

    .slider-area{
    height: 180px;
    }
}
@media screen and (max-width: 367px) {
        
        .slider-area{
            height: 220px;
        }
        }
.faq-section{
    margin-top:-60px;
}
</style>
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
</script>