<template>
  <div id="testimonial">
    <div class="testimonials-container">
      <!-- Bootstrap Carousel -->
      <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel" data-interval="500">
        <!-- Carousel Indicators -->
        <ol class="carousel-indicators ">
          <li v-for="(testimonial, index) in testimonials" :key="index"
              :data-target="'#carouselExampleIndicators'"
              :data-slide-to="index"
              :class="{ active: index === 0 }"></li>
        </ol>

        <!-- Carousel Inner -->
        <div class="carousel-inner">
          <div v-for="(testimonial, index) in testimonials" :key="index"
               class="carousel-item" :class="{ active: index === 0 }">
            <div class="testimonial-item">
              <img :src="testimonial.img" class="testimonial-img" :alt="'Testimonial ' + (index + 1)">
              <h3>{{ testimonial.name }}</h3>
              <h4>{{ testimonial.title }}</h4>
              <p>
                <i class="quote-icon-left fa-solid fa-quote-left"></i>
                {{ testimonial.quote }}
                <i class="quote-icon-right fa-solid fa-quote-right"></i>
              </p>
            </div>
          </div>
        </div>

        <!-- Carousel Controls -->
        <!-- <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      testimonials: [
        {
          img: require('../assets/Images/testimonials-1.jpg'),
          name: 'Saul Goodman',
          title: 'Ceo & Founder',
          quote: 'Proin iaculis purus consequat sem cure digni ssim donec porttitora entum suscipit rhoncus. Accusantium quam, ultricies eget id, aliquam eget nibh et. Maecen aliquam, risus at semper.',
        },
        {
          img: require('../assets/Images/testimonials-2.jpg'),
          name: 'Sara Wilsson',
          title: 'Designer',
          quote: 'Export tempor illum tamen malis malis eram quae irure esse labore quem cillum quid cillum eram malis quorum velit fore eram velit sunt aliqua noster fugiat irure amet legam anim culpa.',
        },
        {
          img: require('../assets/Images/testimonials-3.jpg'),
          name: 'Jena Karlis',
          title: 'Store Owner',
          quote: 'Enim nisi quem export duis labore cillum quae magna enim sint quorum nulla quem veniam duis minim tempor labore quem eram duis noster aute amet eram fore quis sint minim.',
        },
        {
          img: require('../assets/Images/testimonials-4.jpg'),
          name: 'Matt Brandon',
          title: 'Freelancer',
          quote: 'Fugiat enim eram quae cillum dolore dolor amet nulla culpa multos export minim fugiat minim velit minim dolor enim duis veniam ipsum anim magna sunt elit fore quem dolore labore illum veniam.',
        },
        {
          img: require('../assets/Images/testimonials-5.jpg'),
          name: 'John Larson',
          title: 'Entrepreneur',
          quote: 'Quis quorum aliqua sint quem legam fore sunt eram irure aliqua veniam tempor noster veniam enim culpa labore duis sunt culpa nulla illum cillum fugiat legam esse veniam culpa fore nisi cillum quid.',
        },
      ],
    };
  },
};
</script>
