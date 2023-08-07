---
layout: default
permalink: /testimonial/
title: Testimonials
description: "Testimonials What our clients say&#8230;. Don’t take our word for it. Listen to what our clients have to say before you come on board with us for your next project! Founder of Truly Tea. Nyoli Scobie   Byron Bay, NSW, Australia.Hello, my name is Nyoli. I am the owner of Truly Tea in Byron Bay, [&hellip;]"

hero_background_image: "assets/img/slider/testimonials_hero_background_image.webp"
hero_second_image: "assets/img/slider/testimonials_second_image.webp"
hero_hedding_one: Testimonials
hero_hedding_one_font_size: 48px
hero_background_color: rgba(16, 42, 84, 0.8)
opacity: 0.8

animation1: hedding-animation
animation2: hero_second_image-animation

background_color: '#E7EDF8'
status: 'breadcrumb'

testimonials:
  hedding: WHAT OUR CLIENTS SAY....
  description_title: Don’t take our word for it. Listen to what our clients have to say before you come on board with us for your next project!
  description_title_font_size: 18px
  my_class1: d-flex justify-content-center

contact:
  background: "#E7EDF8"
---

{% include header.html %}

<main>
<style>
    @media screen and (max-width: 991px) {
 

  .slider-area{
    height: 122px;
  }


}
</style>
    {% include slider.html %}
    <div style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
    </div>
    {% include services.html %}
    {% include contact.html %}
</main>