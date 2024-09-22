<script>
export default {
  name: 'AppHeader',
};
</script>

<template>
    <header class="app-header">
    <nav class="navbar">
      <div class="logo">
        <img src="../assets/takeout-logo.png" alt="Avada Takeout Logo" />
      </div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">Order Online</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </nav>
    <div class="hero-content">
      <h1>Hungry? <br /> <span>Great Food Delivered</span></h1>
      <button class="cta-button">View Our Menu</button>
    </div>
  </header>
</template>

<style lang="scss">
@import '../assets/scss/AppHeader.scss';
</style>