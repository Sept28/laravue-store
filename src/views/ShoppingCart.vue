<template>
  <div class="shopping">
    <HeaderShayna />

    <div class="breacrumb-section">
      <div class="container">
        <div class="row">
          <div class="col-lg-12 text-left">
            <div class="breadcrumb-text product-more">
              <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
              <span>Shopping Cart</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <section class="shopping-cart spad">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="cart-table">
              <table>
                <thead>
                  <tr>
                    <th>Image</th>
                    <th class="p-name">Product Name</th>
                    <th>Price</th>
                    <th>Quantity</th>
                    <th>Total</th>
                    <th><i class="ti-close"></i></th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="cart-pic first-row">
                      <img src="img/cart-page/product-1.jpg" alt="" />
                    </td>
                    <td class="cart-title first-row">
                      <h5>Pure Pineapple</h5>
                    </td>
                    <td class="p-price first-row">$60.00</td>
                    <td class="qua-col first-row">
                      <div class="quantity">
                        <div class="pro-qty">
                          <input type="text" value="1" />
                        </div>
                      </div>
                    </td>
                    <td class="total-price first-row">$60.00</td>
                    <td class="close-td first-row"><i class="ti-close"></i></td>
                  </tr>
                  <tr>
                    <td class="cart-pic">
                      <img src="img/cart-page/product-2.jpg" alt="" />
                    </td>
                    <td class="cart-title">
                      <h5>American lobster</h5>
                    </td>
                    <td class="p-price">$60.00</td>
                    <td class="qua-col">
                      <div class="quantity">
                        <div class="pro-qty">
                          <input type="text" value="1" />
                        </div>
                      </div>
                    </td>
                    <td class="total-price">$60.00</td>
                    <td class="close-td"><i class="ti-close"></i></td>
                  </tr>
                  <tr>
                    <td class="cart-pic">
                      <img src="img/cart-page/product-3.jpg" alt="" />
                    </td>
                    <td class="cart-title">
                      <h5>Guangzhou sweater</h5>
                    </td>
                    <td class="p-price">$60.00</td>
                    <td class="qua-col">
                      <div class="quantity">
                        <div class="pro-qty">
                          <input type="text" value="1" />
                        </div>
                      </div>
                    </td>
                    <td class="total-price">$60.00</td>
                    <td class="close-td"><i class="ti-close"></i></td>
                  </tr>
                </tbody>
              </table>
            </div>
            <div class="row">
              <div class="col-lg-4 offset-lg-4">
                <div class="proceed-checkout text-left">
                  <ul>
                    <li class="subtotal">Subtotal <span>$240.00</span></li>
                    <li class="cart-total">Total <span>$240.00</span></li>
                  </ul>
                  <router-link to="/success"><a href="#" class="proceed-btn">PROCEED TO CHECK OUT</a></router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import HeaderShayna from '@/components/HeaderShayna.vue'

export default {
  name: "ShoppingCart",
  components: {
    HeaderShayna
  }
}
</script>