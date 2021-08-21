<template>
  <div class="product">
    <HeaderShayna />

    <div class="breacrumb-section text-left">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more">
              <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img
                    class="product-big-img"
                    :src="gambar_default"
                    alt=""
                  />
                  <div class="zoom-icon">
                    <i class="fa fa-search-plus"></i>
                  </div>
                </div>
                <div class="product-thumbs">
                  <carousel class="product-thumbs-track ps-slider" :dots="false" :nav="false">
                    <div
                      class="pt"
                      @click="changeImage(thumbs[0])"
                      :class="thumbs[0] == gambar_default ? 'active' : '' "
                    >
                      <img src="img/product-single/Heels-1.jpg" alt="" />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(thumbs[1])"
                      :class="thumbs[1] == gambar_default ? 'active' : '' "
                    >
                      <img src="img/product-single/Heels-2.jpg" alt="" />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(thumbs[2])"
                      :class="thumbs[2] == gambar_default ? 'active' : '' "
                    >
                      <img src="img/product-single/Heels-3.jpg" alt="" />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(thumbs[3])"
                      :class="thumbs[3] == gambar_default ? 'active' : '' "
                    >
                      <img src="img/product-single/Heels-4.jpg" alt="" />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>oranges</span>
                    <h3>Pure Pineapple</h3>
                    <a href="#" class="heart-icon"
                      ><i class="icon_heart_alt"></i
                    ></a>
                  </div>
                  <div class="pd-rating">
                    <i class="fa fa-star"></i>
                    <i class="fa fa-star"></i>
                    <i class="fa fa-star"></i>
                    <i class="fa fa-star"></i>
                    <i class="fa fa-star-o"></i>
                    <span>(5)</span>
                  </div>
                  <div class="pd-desc">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit.
                      Corporis, error officia. Rem aperiam laborum voluptatum
                      vel, pariatur modi hic provident eum iure natus quos non a
                      sequi, id accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                      Quam possimus quisquam animi, commodi, nihil voluptate
                      nostrum neque architecto illo officiis doloremque et
                      corrupti cupiditate voluptatibus error illum. Commodi
                      expedita animi nulla aspernatur. Id asperiores blanditiis,
                      omnis repudiandae iste inventore cum, quam sint molestiae
                      accusamus voluptates ex tempora illum sit perspiciatis.
                      Nostrum dolor tenetur amet, illo natus magni veniam quia
                      sit nihil dolores. Commodi ratione distinctio harum
                      voluptatum velit facilis voluptas animi non laudantium, id
                      dolorem atque perferendis enim ducimus? A exercitationem
                      recusandae aliquam quod. Itaque inventore obcaecati, unde
                      quam impedit praesentium veritatis quis beatae ea atque
                      perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00 <span>629.99</span></h4>
                  </div>
                  <div class="quantity">
                    <div class="pro-qty">
                      <input type="text" value="1" />
                    </div>
                    <router-link to="/cart"><a href="#" class="primary-btn pd-cart">Add To Cart</a></router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <RelatedShayna />

    <FooterShayna />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from '@/components/HeaderShayna.vue'
import RelatedShayna from '@/components/RelatedShayna.vue'
import FooterShayna from '@/components/FooterShayna.vue'

import carousel from "vue-owl-carousel"

export default {
  name: 'Product',
  components: {
    HeaderShayna,
    RelatedShayna,
    FooterShayna,
    carousel
  },
  data() {
    return {
      gambar_default: "img/product-single/Heels-1.jpg",
      thumbs: [
        "img/product-single/Heels-1.jpg",
        "img/product-single/Heels-2.jpg",
        "img/product-single/Heels-3.jpg",
        "img/product-single/Heels-4.jpg"
      ]
    }
  },
  methods: {
    changeImage(urlImage) {
      this.gambar_default = urlImage;
    }
  },
}
</script>

<style scoped>
  .product-pic-zoom img{
    max-height: 650px;
  }
  .product-thumbs .pt{
    margin-right: 14px;
  }
</style>