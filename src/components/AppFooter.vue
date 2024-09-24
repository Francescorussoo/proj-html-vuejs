<template>
  <footer class="app-footer">
    <div class="footer-top">
      <div class="footer-column">
        <h3>Order Online</h3>
        <ul>
          <li>Appetizers</li>
          <li>Burgers</li>
          <li>Pizza</li>
          <li>Fries</li>
          <li>Sides</li>
          <li>Desserts</li>
          <li>Beverages</li>
          <li>Specials</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>Navigate</h3>
        <ul>
          <li><span>Home</span></li>
          <li>Alternate Home</li>
          <li>Menu</li>
          <li>About</li>
          <li>News</li>
          <li>Contact Us</li>
          <li>Cart</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>Information</h3>
        <ul>
          <li>My Account</li>
          <li>Terms Of Service</li>
          <li>Privacy Policy</li>
        </ul>
        <div class="store-buttons">
          <img src="../assets/app-store-badge-200x67.png" alt="Download on the App Store" />
          <img src="../assets/play-store-badge-200x67.png" alt="Get it on Google Play" />
        </div>
      </div>
      <div class="footer-column">
        <h3>Opening Hours</h3>
        <ul>
          <li>Mon – <span>10AM to 11PM</span></li>
          <li>Tue – <span>10AM to 11PM</span></li>
          <li>Wed – <span>10AM to 11PM</span></li>
          <li>Thur – <span>10AM to 11PM</span></li>
          <li>Fri – <span>10AM to 11PM</span></li>
          <li>Sat – <span>10AM to 1AM</span></li>
          <li>Sun – <span>11AM to 10PM</span></li>
        </ul>
      </div>
      <div class="footer-column voucher-column">
        <h3>Voucher</h3>
        <img src="../assets/footer-coupon-200x200.png" alt="20% Off Coupon" class="voucher-img" />
        <p>Just Use The Code</p>
        <strong>FIRSTORDER</strong>
        <p>At Checkout</p>
      </div>
    </div>
    <div class="footer-bottom">
      <img src="../assets/takeout-logo.png" alt="Avada Takeout Logo" class="footer-logo"/>
      <h2>Stay In The Loop</h2>
      <p>Sign up to receive up to date news and offers directly in your inbox:</p>
      <form>
        <input type="email" placeholder="you@email.com" />
        <button type="submit">Subscribe</button>
      </form>
      <div class="social-icons">
        <i class="fa-brands fa-facebook-f"></i>
        <i class="fa-brands fa-x-twitter"></i>
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-linkedin"></i>
        <i class="fa-solid fa-wifi"></i>
        <i class="fa-brands fa-youtube"></i>
        <i class="fa-regular fa-message"></i>
      </div>
      <p class="copyright"><span>&copy;Copyright 2021 - 2020|Avada Theme by</span> Theme Fusion<span>|All Right Reserved|Powered By</span>WordPress</p>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@import '../assets/scss/AppFooter.scss';
</style>
