<template>
  <div class="sub-root">
    <header class="header">
      <router-link to="/">
        <img
          alt="App logo"
          class="logo"
          src="@/assets/weather-icon.svg"
          width="200"
          height="200"
        />
      </router-link>

      <div class="wrapper">
        <RouterLink class="wrapper_link" to="/">Home</RouterLink>
        <RouterLink class="wrapper_link" to="/weather">Weather</RouterLink>
      </div>
    </header>
    <RouterView />
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang="scss" scoped>
.sub-root {
  display: flex;
  flex-direction: column;
}

.header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.wrapper_link {
  padding: 5px;
  margin-left: 30px;
  font-size: 30px;
  color: white;
  text-decoration: none;
}

.wrapper_link:first-child {
  margin: 0;
}
</style>

<style lang="scss" scoped>
@use "@/assets/global";

.scss-class {
  background-color: blue;
  font: 100% global.$font-stack;
  color: global.$primary-color;
}

.wrapper_link:hover {
  background-color: global.$link-color;
}
</style>
