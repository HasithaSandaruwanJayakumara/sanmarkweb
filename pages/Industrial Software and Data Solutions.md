---
layout: default
permalink: /industrial-solutions/
title: Industrial Software and Data Solutions

hero_background_image: "assets/img/slider/service_hero_background_image.webp.webp"
hero_second_image: "assets/img/slider/service_second_image.webp"
hero_hedding_one: "Software Development Industrial Solutions for Any Industry"
hero_paragraph: 'Are you on the lookout for a software development company that can give you industrial solutions, but are unsure if they are familiar with the nitty-gritty of your specific industry? Wonder no more!'
hero_paragraph_two: 'The team at Sanmark Solutions, has been in software development for businesses for a number of years, with over 500 projects under our belt. We have immense experience working in diverse industries and creating software solutions for diverse business models, which means we are your best option when it comes to industrial solutions for Melbourne & Sydney based businesses, like software, applications and industrial data solutions.'
hero_hedding_one_font_size: 38px
hero_hedding_two_font_size: 20px
hero_background_color: rgba(16, 42, 84, 0.8)
hero_other_slider_content: other-slider-content
hero_id: other_hero_section_two
opacity: 0.8

animation1: hedding-animation
animation2: hero_second_image-animation

background_color: '#E7EDF8'
status: 'breadcrumb' 

recent_project: 
  text:  "…and many more!"
  class_one: recent-projects-active
  class_two: carousel-title-text
  background_color: '#E7EDF8'

portfolio_status: portfolios carousel

intro:
  title: "INDUSTRIAL SOLUTIONS"
  hedding: "Why is it important for a software developer to have experience in diverse industries?"
  content: "two_paragraph"
  image: "assets/img/Industrial Software and Data Solutions/industrial-solutions.webp"
  status: "double-circle"
  class: "intro_div"

intro_two: 
  title: "<span class='bullet_ltr'>INDUSTRIES</span>"
  hedding: "<span class='bullet_ltr'>Industries we are familiar with</span>"
  content: "two_paragraph"
  paragraph_one: "<span class='bullet_ltr'>At Sanmark Solutions we have worked in many industries over the past years, creating software solutions that boost business growth. We have built software industrial solutions for common tasks carried out by many businesses, and this cross-industry experience helps us to tweak our existing solutions to suit your specific industry requirements, which means that you can get a solution in double quick time.</span>"
  paragraph_two: "<span class='bullet_ltr'>Some specific industries we have worked in include (but not limited to):</span>"
  class: "intro_div"
  class_two: '#ffffff'
  class_three: 'rtl'
  ltr_bullet_class: 'direction: ltr;'
  image: "assets/img/Industrial Software and Data Solutions/industrial-solutions-2.webp"

intro_three:
  title: "SOLUTIONS"
  hedding: "What Type of Industrial Solutions We Can Do For You"
  paragraph_one: "We have created unique software solutions and industrial solutions for Melbourne & Sydney businesses, including:"
  paragraph_four: "We have developed hundreds of core solutions for many industries and we can adjust these to suit your specific business needs and requirements, providing you with the exact solution you need, only faster."
  content: "paragraph"
  image: "assets/img/Industrial Software and Data Solutions/industrial-solutions-3.webp"
  status: "double-circle"
  class: "intro_div"
   

  
landmark:
    image: "assets/img/bg/landmark2.webp"
    image_align: "d-flex justify-content-center"
    image_width: 330
    image_height: 330
    description_line1: Be One of the Satisfied
    description_line2: Sanmark Clients
    description_line3: in Australia
    join: Join Now

values:
  hedding_two: Why Choose Us for Industrial Solutions Software Development?
  first_main_paragraph: "There are many reasons why Sanmark Solutions is your best choice when it comes to choosing a software company for industrial solutions. Here are just a few reasons why you should choose us."

  
faq:
  title: "FAQ"
  hedding: "Frequently Asked Questions"
  image: "/assets/images/faq.webp"
  content: "expanded"
  status: "one-circle"
  image: "assets/img/faq.webp"

# SEO
description: 'Industrial solutions that address your specific business needs by professional software developers with diverse industry experience. Contact us today!'
---

{% include header.html %}
{% include slider.html %}

<div style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
    </div>

{% include intro_section.html links=site.data.intro_bullets.industrial_solutions title=page.intro.title hedding=page.intro.hedding 
      paragraph_one=page.intro.paragraph_one paragraph_two=page.intro.paragraph_two image=page.intro.image status=page.intro.status paragraph_four=page.intro.paragraph_four content=page.intro.content class=page.intro.class %}

{% include intro_section.html links=site.data.intro_bullets.industrial_solutions_industries title=page.intro_two.title hedding=page.intro_two.hedding image=page.intro_two.image content=page.intro_two.content class=page.intro_two.class background_color=page.intro_two.class_two rtl_class=page.intro_two.class_three status=page.intro.status paragraph_one=page.intro_two.paragraph_one paragraph_two=page.intro_two.paragraph_two paragraph_three=page.intro_two.paragraph_three paragraph_four=page.intro_two.paragraph_four ltr_bullet_class=page.intro_two.ltr_bullet_class %}

{% include intro_section.html links=site.data.intro_bullets.industrial_solutions_solutions title=page.intro_three.title hedding=page.intro_three.hedding 
      paragraph_one=page.intro_three.paragraph_one paragraph_four=page.intro_three.paragraph_four image=page.intro_three.image status=page.intro_three.status paragraph_four=page.intro_three.paragraph_four content=page.intro_three.content class=page.intro_three.class %}

{% include call_to_action.html %}

{% include values.html links=site.data.values.Industria_software_and_Data_solutions hedding_two=page.values.hedding_two paragraph_one=page.values.first_main_paragraph paragraph_two=page.values.second_main_paragraph paragraph_three=page.values.third_main_paragraph %}

{% include testimonials.html %}

{% include portfolios.html links=site.data.successStorices class_one=page.recent_project.class_one class_two=page.recent_project.class_two text=page.recent_project.text %}

{% include contact.html %}
{% include intro_section.html link=site.data.colapse_data.colapseData_isds title=page.faq.title hedding=page.faq.hedding image=page.faq.image content=page.faq.content status=page.faq.status%}

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

  function setCardHeights() {
      // Reset card heights
      $('.value-card').height('auto');

      // Initialize variables
      let maxHeight = 0;

      // Find the maximum height among the cards
      $('.value-card').each(function () {
        const cardHeight = $(this).outerHeight();
        maxHeight = Math.max(maxHeight, cardHeight);
      });

      // Set the maximum height to all the cards
      $('.value-card').height(maxHeight);
    }

    // Call the function initially and on window resize
    $(window).on('load resize', function () {
      setCardHeights();
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
