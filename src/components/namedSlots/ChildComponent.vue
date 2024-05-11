<template>
  <div>
    <header>
      <slot name="header"></slot>
      <div>Hello From Header in Child</div>
    </header>
    <footer>
      <slot name="footer"></slot>
      <div>Hello From Footer in Child</div>
    </footer>
  </div>
</template>