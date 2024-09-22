<template>
    <main class="app-main">
        
      <section class="info-links">
        <div class="info-item">
          <i class="fas fa-clock"></i>
          <span>24/7 Delivery</span>
        </div>
        <div class="info-item">
          <i class="fas fa-hamburger"></i>
          <span>Over 100 Dishes</span>
        </div>
        <div class="info-item">
          <i class="fas fa-mobile-alt"></i>
          <span>In App Ordering</span>
        </div>
        <div class="info-item">
          <i class="fas fa-car"></i>
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
    </main>
  </template>
  
  <script>
  import skinOnFries from '../assets/skin-on-fries-210x300.jpg';
  import chocoCookieFrappe from '../assets/choco-cookie-frappe-210x300.jpg';
  import donutBurger from '../assets/donut-burger-210x300.jpg';
  
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
      };
    },
  };
  </script>
  
  <style scoped lang="scss">
  .app-main {
    padding: 20px;
    text-align: center;
  
    .info-links {
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 20px 0;
  
      .info-item {
        display: flex;
        align-items: center;
        font-size: 14px;
        color: #333;
        
        i {
          margin-right: 8px;
          font-size: 18px;
        }
      }
    }
  
    .popular-dishes {
      margin: 0 auto;
      max-width: 1200px;
  
      h2 {
        font-size: 28px;
        margin-bottom: 20px;
      }
  
      .dishes {
        display: flex;
        justify-content: space-around;
        gap: 20px;
  
        .dish {
          max-width: 250px;
          text-align: center;
  
          img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
          }
  
          h3 {
            margin: 10px 0;
            font-size: 18px;
            font-weight: bold;
          }
  
          p {
            color: #ec4858;
          }
        }
      }
  
      .order-button {
        margin-top: 20px;
        padding: 10px 20px;
        background-color: #ec4858;
        color: #fff;
        border: none;
        cursor: pointer;
        border-radius: 5px;
        font-size: 16px;
        transition: background-color 0.3s;
  
        &:hover {
          background-color: #ec4858;
        }
      }
    }
  }
  </style>
  