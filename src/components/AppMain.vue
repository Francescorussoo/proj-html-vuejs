<template>
  <main class="app-main">
    <section class="info-links">
      <div class="info-item">
        <i class="fa-regular fa-clock"></i>
        <span>24/7 Delivery</span>
      </div>
      <div class="info-item">
        <i class="fa-solid fa-burger"></i>
        <span>Over 100 Dishes</span>
      </div>
      <div class="info-item">
        <i class="fa-solid fa-mobile-screen-button"></i>
        <span>In App Ordering</span>
      </div>
      <div class="info-item">
        <i class="fa-solid fa-car"></i>
        <span>Fast Delivery</span>
      </div>
    </section>

    <section class="popular-dishes">
      <h2>Our Most Popular Dishes</h2>
      <div class="dishes">
        <div class="dish" v-for="dish in dishes" :key="dish.name">
          <img :src="dish.image" :alt="dish.name" />
          <h3>{{ dish.name }}</h3>
          <p>{{ dish.price }}</p>
        </div>
      </div>
      <button class="order-button">Start Your Order</button>
    </section>

    <section class="banner">
      <img src="../assets/first-order-background-scaled.jpg" alt="20% Off Your First Order" />
    </section>

    <section class="menu-categories">
      <div class="categories-header">
        <h2>Menu Categories</h2>
        <button class="view-full-menu">View the Full Menu</button>
      </div>
      <div class="categories-grid">
        <div
          class="category"
          v-for="category in categories"
          :key="category.name"
          :style="{ backgroundImage: `url(${category.image})` }"
        >
          <span class="category-name">{{ category.name }}</span>
        </div>
      </div>
    </section>

    <section class="category-icons">
      <div class="icon-item">
        <i class="fa-solid fa-leaf"></i>
        <span>Vegetarian</span>
      </div>
      <div class="icon-item">
        <i class="fa-solid fa-wheat-awn"></i>
        <span>Gluten Free</span>
      </div>
      <div class="icon-item">
        <i class="fa-solid fa-bottle-droplet"></i>
        <span>Dairy Free</span>
      </div>
      <div class="icon-item">
        <i class="fa-solid fa-bacon"></i>
        <span>Keto Friendly</span>
      </div>
    </section>
    <section class="second-banner">
      <div class="banner-content">
       <h2>Download Our <br><span><strong>Ordering App</strong></span></h2>
      <div class="store-buttons">
      <a href="#" class="store-button">
        <img src="../assets/app-store-badge-200x67.png" alt="Download on the App Store" />
      </a>
      <a href="#" class="store-button">
        <img src="../assets/play-store-badge-200x67.png" alt="Get it on Google Play" />
      </a>
      </div>
    </div>
      <img src="../assets/app-ordering-scaled.jpg" alt="App Ordering Banner" />
    </section>
    <section class="latest-news">
     <div class="news-header">
      <h2>Latest News</h2>
    <button class="read-more-news">Read More News</button>
    </div>
    <div class="news-grid">
     <div class="news-item">
      <img src="../assets/pancake-burger-600x450.jpg" alt="Pancake Burger">
      <h3>NEW: The Pancake Burger</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi.</p>
     </div>
    <div class="news-item">
      <img src="../assets/new-milkshake-menu-600x450.jpg" alt="New Milkshake Menu">
      <h3>New Milkshake Menu</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi.</p>
    </div>
    </div>
    </section>
  </main>
</template>

<script>
import skinOnFries from '../assets/skin-on-fries-210x300.jpg';
import chocoCookieFrappe from '../assets/choco-cookie-frappe-210x300.jpg';
import donutBurger from '../assets/donut-burger-210x300.jpg';

import appetizers from '../assets/appetizers-menu-background.jpg';
import burgers from '../assets/burgers-menu-background.jpg';
import pizzas from '../assets/pizza-menu-background.jpg';
import fries from '../assets/fries-menu-background.jpg';
import sides from '../assets/sides-menu-background.jpg';
import desserts from '../assets/desserts-menu-background.jpg';
import beverages from '../assets/beverages-menu-background.jpg';
import specials from '../assets/specials-menu-background.jpg';

export default {
  name: 'AppMain',
  data() {
    return {
      dishes: [
        {
          name: 'Skin On Fries',
          price: '$3.00 - $6.00',
          image: skinOnFries,
        },
        {
          name: 'Choco Cookie Frappe',
          price: '$4.99',
          image: chocoCookieFrappe,
        },
        {
          name: 'The Donut Burger',
          price: '$6.99',
          image: donutBurger,
        },
      ],
      categories: [
        { name: 'Appetizers', image: appetizers },
        { name: 'Burgers', image: burgers },
        { name: 'Pizzas', image: pizzas },
        { name: 'Fries', image: fries },
        { name: 'Sides', image: sides },
        { name: 'Desserts', image: desserts },
        { name: 'Beverages', image: beverages },
        { name: 'Specials', image: specials },
      ],
    };
  },
};
</script>

<style lang="scss">
@import '../assets/scss/AppMain.scss';
</style>
