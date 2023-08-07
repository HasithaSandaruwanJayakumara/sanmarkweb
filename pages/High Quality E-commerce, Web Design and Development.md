---
layout: default
permalink: /web-development/
title: High Quality E-commerce, Web Design and Development services

hero_background_image: "assets/img/slider/web_design_servicepage_hero_background_image.webp"
hero_second_image: "assets/img/slider/hero-second-image.webp"
hero_hedding_one: "High Quality E-commerce, Web Design and Development services"
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

contact:
  background: "#E7EDF8"
intro:
  content: "call_to_action_contact"
  image: "assets/img/web_development/web_development.webp"
  paragraph_one: "Having a robust website is the key to the success of any business. We offer design, development, integration and maintenance of your website, perfected to meet all your needs and standards."
  button:  "Let's Talk to Kick-start Your Success"
  class: "intro_div"
  heading_one: "What is a good website?"
  heading_one_paragraph: "Your website is your best channel to make a lasting impression on your potential customers even before their decision making process. However, there are over 600 million websites currently online on the internet, which put you in an extremely competitive ground to stand out from the rest. A good website gives a strong and clear message to the visitor, has an attractive and pleasant user interface for them to easily navigate through and it has great content that gives value for your visitors."
  heading_two: "Why hire Sanmark for your next web development project?"
  heading_two_paragraph_one: "As you can see in our portfolio, we have done a variety of web development projects for many different industries and for clients all around the world. Our main target in creating a website is to make it stand out in the best way, while giving a clear message to the visitor on what the website is about. We know that it’s not always about gimmicks and a plenty of colors and the simplicity is the best, however, we are not afraid to use attractive templates that keeps your visitors coming back too."
  heading_two_paragraph_two: "Let it be a simple blog to promote your story or a business website for a mid to corporate level company, Sanmark team will give your project undivided attention and effort until you get what you seek for!"
  heading_three: "Our Promise"
  heading_three_list_item_one : "High Security"
  heading_three_list_item_two : "Better Conversion Rates"
  heading_three_list_item_three : "Wider reach"
  heading_three_list_item_four : "User friendly interface"
  heading_three_list_item_five : "Easy maintainability"



# SEO
description: 'We are at Sanmark provide professional and high quality E-commerce development, web design and web development services for affordable price.'

---

{% include header.html %}
{% include slider.html %}

<div style="margin-top:-50px; background-color:{{page.background_color}};" >
    <div style="height:50px"></div>
    </div>

{% include intro_section.html  title=page.intro.title hedding=page.intro.hedding
      paragraph_one=page.intro.paragraph_one button=page.intro.button heading_one=page.intro.heading_one heading_one_paragraph=page.intro.heading_one_paragraph heading_two=page.intro.heading_two
      heading_two_paragraph_one=page.intro.heading_two_paragraph_one heading_two_paragraph_two=page.intro.heading_two_paragraph_two heading_three=page.intro.heading_three 
      heading_three_list_item_one=page.intro.heading_three_list_item_one
      heading_three_list_item_two=page.intro.heading_three_list_item_two 
      heading_three_list_item_three=page.intro.heading_three_list_item_three
      heading_three_list_item_four=page.intro.heading_three_list_item_four
      heading_three_list_item_five=page.intro.heading_three_list_item_five
      image=page.intro.image status=page.intro.status  content=page.intro.content class=page.intro.class %}


{% include testimonials.html %}

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
