<template lang="pug">
v-app
  v-main
    router-view
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style>
@font-face {
  font-family: 'Nike Futura';
  src: url('assets/fonts/Nike-Futura.woff2');
}
@font-face {
  font-family: 'Nike TG';
  src: url('assets/fonts/Nike-TG.woff2');
}
*{
  font-family: "Helvetica Neue",
    Helvetica,
    Arial,
    sans-serif;
}

a {
  text-decoration: none;
}

h1,h2,h3,h4,h5,h6,p,a{
  color: #111;
}
</style>
