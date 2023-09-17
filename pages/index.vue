<template>
  <div style="overflow-x: hidden">
    <Header title="Home"></Header>

    <section class="bg-section">
      <div class="container">
        <div class="row home-sections justify-content-end">
          <div class="col-lg-6 order-lg-last"
               data-aos="fade-left"
               data-aos-duration="1000">
            <h3 class="main-title">卡片一</h3>
            <p>这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
            <a class="primary-button"
               href="description">了解更多(超链接)</a>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="row home-sections">
          <div class="col-lg-6"
               data-aos="fade-right"
               data-aos-duration="1000">
            <h3 class="main-title">卡片二</h3>
            <p>这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
            <br>
            <p>这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
          </div>
          <PieChart />
        </div>
      </div>
    </section>

    <section class="stats-counter">
      <div class="container">
        <div class="row">
          <div class="col-lg-4 count"
               data-aos="zoom-in"
               data-aos-duration="1000">
            <div class="count-icon">
              <img src="https://static.igem.wiki/teams/4118/wiki/icons/counter-first.png"
                   width="150"
                   height="150"
                   alt="#1 cause of cancer deaths">
            </div>
            <div class="number">卡片一</div>
            <span>这是一段解释</span>
          </div>
          <div class="col-lg-4 count"
               data-aos="zoom-in"
               data-aos-duration="1000">
            <div class="count-icon">
              <img src="https://static.igem.wiki/teams/4118/wiki/icons/counter-cases.png"
                   width="150"
                   height="150"
                   alt="2.2 million new cases worldwide annually">
            </div>
            <div class="number">卡片二</div>
            <span>这是一段解释</span>
          </div>
          <div class="col-lg-4 count"
               data-aos="zoom-in"
               data-aos-duration="1000">
            <div class="count-icon">
              <img src="https://static.igem.wiki/teams/4118/wiki/icons/counter-deaths.png"
                   width="150"
                   height="150"
                   alt="1.8 million new deaths worldwide annually">
            </div>
            <div class="number">卡片三</div>
            <span>这是一段解释</span>
          </div>
        </div>
      </div>
    </section>

    <section class="grid-transparent-cards">
      <div data-aos="fade-up"
           data-aos-duration="1000">
        <h3 class="large-title">展览板</h3>
        <p class="smaller"
           style="text-align: center !important;">
          这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-lg-4"
               data-aos="fade-up-right"
               data-aos-duration="1000">
            <div class="card-component">
              <div class="comp">
                <img src="https://static.igem.wiki/teams/4118/wiki/icons/biopsies-icon.png"
                     alt="" />
              </div>
              <h4 class="small-title2">卡片一</h4>
              <h5 class="excerpt">这是一段标题</h5>
              <p> 这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>

            </div>
          </div>
          <div class="col-lg-4"
               data-aos="fade-up"
               data-aos-duration="1000">
            <div class="card-component">
              <div class="comp">
                <img src="https://static.igem.wiki/teams/4118/wiki/icons/circrna-icon.png"
                     alt="" />
              </div>
              <h4 class="small-title2">卡片二</h4>
              <h5 class="excerpt">这是一段标题</h5>
              <p> 这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
            </div>
          </div>
          <div class="col-lg-4"
               data-aos="fade-up-left"
               data-aos-duration="1000">
            <div class="card-component">
              <div class="comp">
                <img src="https://static.igem.wiki/teams/4118/wiki/icons/dna-icon.png"
                     alt="" />
              </div>
              <h4 class="small-title2">卡片三</h4>
              <h5 class="excerpt">这是一段标题</h5>
              <p> 这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落，这是一个很长的段落</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="container-fluid">
      <div class="row">
        <div class="col tabbed-gallery">
          <ul class="thumbnails">
            <li>
              <input type="radio"
                     name="select"
                     id="image1"
                     checked>
              <div class="item-hugger"
                   data-aos="fade-up"
                   data-aos-duration="1000">
                <img class="thumb-image"
                     src="https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/wet-lab-small.jpg" />
                <label for="image1"></label>
              </div>
              <div class="gal-content"
                   style="background: url('https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/wet1.jpg') center center no-repeat; background-size: cover;">
                <div class="item-wrapper"
                     data-aos="fade-right"
                     data-aos-duration="1000">
                  <div class="title">卡片一</div>
                  <p class="txt">这是一段很长的介绍，这是一段很长的介绍</p>
                  <a href="experiments"
                     class="pills">超链接，指向相关页面</a>
                </div>
              </div>
            </li>
            <li>
              <input type="radio"
                     name="select"
                     id="image2">
              <div class="item-hugger"
                   data-aos="fade-up"
                   data-aos-duration="1000">
                <img class="thumb-image"
                     src="https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/product-small.jpg" />
                <label for="image2"></label>
              </div>
              <div class="gal-content"
                   style="background: url('https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/product1.jpg') center center no-repeat; background-size: cover;">
                <div class="item-wrapper"
                     data-aos="fade-right"
                     data-aos-duration="1000">
                  <div class="title">卡片二</div>
                  <p class="txt">这是一段很长的介绍，这是一段很长的介绍</p>
                  <a href="implementation"
                     class="pills">超链接，指向相关页面</a>
                </div>
              </div>
            </li>
            <li>
              <input type="radio"
                     name="select"
                     id="image3">
              <div class="item-hugger"
                   data-aos="fade-up"
                   data-aos-duration="1000">
                <img class="thumb-image"
                     src="https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/hp-small.jpg" />
                <label for="image3"></label>
              </div>
              <div class="gal-content"
                   style="background: url('https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/hp1.jpg') center center no-repeat; background-size: cover;">
                <div class="item-wrapper"
                     data-aos="fade-right"
                     data-aos-duration="1000">
                  <div class="title">卡片三</div>
                  <p class="txt">这是一段很长的介绍，这是一段很长的介绍</p>
                  <a href="human-practices"
                     class="pills">超链接，指向相关页面</a>
                </div>
              </div>
            </li>
            <li>
              <input type="radio"
                     name="select"
                     id="image4">
              <div class="item-hugger"
                   data-aos="fade-up"
                   data-aos-duration="1000">
                <img class="thumb-image"
                     src="https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/e-sc-lab-horizontal.jpg" />
                <label for="image4"></label>
              </div>
              <div class="gal-content"
                   style="background: url('https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/e-c1.jpg') center center no-repeat; background-size: cover;">
                <div class="item-wrapper"
                     data-aos="fade-right"
                     data-aos-duration="1000">
                  <div class="title">卡片四</div>
                  <p class="txt">这是一段很长的介绍，这是一段很长的介绍</p>
                  <a href="communication"
                     class="pills">超链接，指向相关页面</a>
                </div>
              </div>
            </li>
            <li>
              <input type="radio"
                     name="select"
                     id="image5">
              <div class="item-hugger"
                   data-aos="fade-up"
                   data-aos-duration="1000">
                <img class="thumb-image"
                     src="https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/model-small.jpg" />
                <label for="image5"></label>
              </div>
              <div class="gal-content"
                   style="background: url('https://static.igem.wiki/teams/4118/wiki/website-assets/home-gallery/model1.jpg') center center no-repeat; background-size: cover;">
                <div class="item-wrapper"
                     data-aos="fade-right"
                     data-aos-duration="1000">
                  <div class="title">卡片五</div>
                  <p class="txt">这是一段很长的介绍，这是一段很长的介绍</p>
                  <a href="model"
                     class="pills">超链接，指向相关页面</a>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  mounted () {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 1000)
    })
    AOS.init({});
  },
}
</script>
