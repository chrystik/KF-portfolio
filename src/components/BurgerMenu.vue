<template>
  <div class="burger">
      <div :class="{ active: isActive }" @click="isActive = !isActive" class="burger-arrow">
        <span></span>
        <span></span>
      </div>
      <div :class="{ active: isActive }" class="burger-menu">
        <router-link to="/" class="menu-link">Home</router-link>
        <router-link to="/about" class="menu-link">About</router-link>
        <router-link to="/works" class="menu-link">Works</router-link>
        <router-link to="/contacts" class="menu-link">Contacts</router-link>
      </div>
  </div>
</template>

<script>
export default {
  name: "BurgerMenu",
  data() {
    return {
      isActive: false
    }
  }
};
</script>

<style scoped>

  .burger-arrow {
    position: fixed;
    top: 50%;
    transform: translateY(-50%);
    right: 50px;
    width: 30px;
    height: 40px;
    cursor: pointer;
    z-index: 2;
    transition: 1s;
  }

  .burger-arrow span{
    position: absolute;
    left: 0;
    display: block;
    width: 20px;
    height: 3px;
    border-radius: 3px;
    background-color: #0e0e0e;
    transition: .5s;
  }

  .burger-arrow span:first-child {
    top: 12px;
    transform: rotate(-45deg);
  }

  .burger-arrow span:last-child {
    bottom: 12px;
    transform: rotate(45deg);
  }

  .burger-menu {
    display: block;
    position: fixed;
    background-color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    border-left: 3px solid #0e0e0e;
    transform: translateX(100%);
    transition: 1s;
  }

  .burger-menu.active {
    transform: translateX(0);
  }

  .burger-arrow.active span:first-child{
    top: 18px;
  }

  .burger-arrow.active span:last-child{
    bottom: 19px;
  }

  .menu-link {
    width: 200px;
    height: 200px;
    background-color: rgb(51, 51, 51);
    border-radius: 20px;
    box-shadow: rgb(0 0 0 / 0%) 0px 0px 20px 0px inset, rgb(0 0 0 / 20%) 0px 0px 20px 0px;
    transition: all 0.3s ease-in 0s;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    color: #0e0e0e;
    font-weight: 600;
    text-decoration: none;
    margin-left: 15px;
    margin-right: 15px;
  }

  .menu-link:hover {
    box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
    transition: all 0.3s ease-in 0s;
  }

  @media (max-width: 1399.98px) {
    .menu-link {
      width: 180px;
      height: 180px;
    }
  }

  @media (max-width: 1199.98px) {
    .burger-arrow {
      right: 30px;
    }

    .menu-link {
      width: 160px;
      height: 160px;
      font-size: 20px;
    }
  }

  @media (max-width: 991.98px) {
    .burger-arrow {
      right: unset;
      left: 50%;
      transform: translateX(-50%) translateY(0) rotate(-90deg);
      top: 0px;
    }

    .burger-menu {
      transform: translateX(0) translateY(-100%);
      border-left: none;
      border-bottom: 3px solid #0e0e0e;
    }

    .burger-menu.active {
      transform: translateY(0);
    }

      .menu-link {
      width: 140px;
      height: 140px;
      font-size: 18px;
    }
  }

  @media (max-width: 767.98px) {
    .menu-link {
      width: 120px;
      height: 120px;
      font-size: 16px;
    }
  }

  @media (max-width: 575.98px) {
    .burger-menu {
      flex-direction: column;
    }

    .menu-link {
      margin-top: 10px;
      margin-bottom: 10px;
    }
  }

</style>
