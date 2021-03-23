<template>
  <nav class="page_nav">
    <ul class="mainmenu">
      <li class="lavel-1">
        <n-link to="/">
          <span>Home</span>
        </n-link>
      </li>
      <li class="lavel-1">
        <n-link to="#">
          <span>Schedule/Book Vaccine</span>
        </n-link>
      </li>
      <li class="lavel-1">
        <n-link to="#">
          <span>Contact Us</span>
        </n-link>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss">
    .mega__list {
        display: flex;
        li {
            flex-basis: 25%;
        }
    }
</style>
