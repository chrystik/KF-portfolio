<template>
  <div class="menu">
    <router-link to="/about" class="menu-link">About</router-link>
    <router-link to="/works" class="menu-link">Works</router-link>
    <router-link to="/contacts" class="menu-link">Contacts</router-link>
  </div>
</template>

<script>

export default {
  name: "Menu",

};
</script>

<style scoped>
.menu {
  width: 700px;
  display: flex;
  justify-content: space-between;
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
}

.menu-link:hover {
  box-shadow: rgb(0 0 0 / 20%) 0px 0px 20px 0px inset, rgb(0 0 0 / 0%) 0px 0px 20px 0px;
  transition: all 0.3s ease-in 0s;
}

@media (max-width: 1399.98px) {
  .menu {
    width: 650px;
  }

  .menu-link {
    width: 180px;
    height: 180px;
  }
}

@media (max-width: 1199.98px) {
  .menu {
    width: 600px;
  }

  .menu-link {
    width: 160px;
    height: 160px;
    font-size: 20px;
  }
}

@media (max-width: 991.98px) {
  .menu {
    width: 500px;
  }

  .menu-link {
    width: 140px;
    height: 140px;
    font-size: 18px;
  }
}

@media (max-width: 767.98px) {
  .menu {
    width: 400px;
  }

  .menu-link {
    width: 120px;
    height: 120px;
    font-size: 16px;
  }
}

@media (max-width: 575.98px) {
  .menu {
    flex-direction: column;
    width: fit-content;
    height: 400px;
  }
}
</style>
