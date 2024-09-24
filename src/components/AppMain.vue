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
      border-radius: 20px;
      font-size: 16px;
      transition: background-color 0.3s;

      &:hover {
        background-color: #d43c4f;
      }
    }
  }

  .banner {
    width: 100vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
    overflow: hidden;
    margin: 20px 0 0;

    img {
      width: 100%;
      height: 340px;
      object-fit: cover;
      display: block;
    }
  }

  .menu-categories {
    margin: 40px 220px;

    .categories-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;

      h2 {
        font-size: 28px;
      }

      .view-full-menu {
        padding: 10px 20px;
        background-color: #ec4858;
        color: #fff;
        border: none;
        cursor: pointer;
        border-radius: 20px;
        font-size: 16px;
        transition: background-color 0.3s;

        &:hover {
          background-color: #d43c4f;
        }
      }
    }

    .categories-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;

      .category {
        position: relative;
        height: 150px;
        background-size: cover;
        background-position: center;
        border-radius: 8px;
        display: flex;
        align-items: center;
        justify-content: center;

        .category-name {
          font-size: 20px;
          color: #fff;
          font-weight: bold;
          text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
        }
      }
    }
  }

  .category-icons {
    display: flex;
    justify-content: center;
    gap: 200px;
    margin-top: 50px;

    .icon-item {
      display: flex;
      flex-direction: column;
      align-items: center;

      i {
        font-size: 40px;
        margin-bottom: 5px;

        &.fa-leaf {
          color: #4caf50;
        }

        &.fa-wheat-awn {
          color: #fbc02d;
        }

        &.fa-bottle-droplet {
          color: #2196f3;
        }

        &.fa-bacon {
          color: #d2691e;
        }
      }

      span {
        margin-top: 5px;
        font-size: 14px;
        color: #333;
      }
    }
  }

  .second-banner {
    width: 100vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
    overflow: hidden;
    margin: 20px 0;
    display: flex;
    align-items: center;
    justify-content: center;

    .banner-content {
      position: absolute;
      left: 15%;
      top: 33%;
      text-align: left;

      h2 {
        font-size: 26px;
        line-height: 1.2;
        color: #fff;
        margin-bottom: 20px;

        span{
        font-size: 50px;
        line-height: 1.2;
        color: #f4b400;
        margin-bottom: 20px;
        }
      }

      .store-buttons {
        display: flex;
        gap: 10px;

        .store-button img {
          width: 150px;
          height: auto;
          transition: transform 0.3s;

          &:hover {
            transform: scale(1.05);
          }
        }
      }
    }

    img {
      width: 100%;
      object-fit: cover;
      display: block;
    }
  }

  .latest-news {
    margin: 40px 0;
    text-align: center;

    .news-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;

      h2 {
        font-size: 28px;
        position: relative;
        left: 345px;
      }

      .read-more-news {
        padding: 10px 20px;
        position: relative;
        right: 340px;
        background-color: #ec4858;
        color: #fff;
        border: none;
        cursor: pointer;
        border-radius: 20px;
        font-size: 16px;
        transition: background-color 0.3s;

        &:hover {
          background-color: #d43c4f;
        }
      }
    }

    .news-grid {
      display: flex;
      gap: 65px;
      justify-content: center;

      .news-item {
        max-width: 30%;
        text-align: center;

        img {
          width: 100%;
          border-radius: 8px;
          margin-bottom: 10px;
        }

        h3 {
          font-size: 22px;
          margin: 10px 0;
          font-weight: bold;
        }

        p {
          font-size: 14px;
          color: #666;
        }
      }
    }
  }
}
</style>
