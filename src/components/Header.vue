<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="col-md-3">
          <h1>Formularios</h1>
        </div>
        <div class="col-md-6">
          <img width="100" :src="url" :alt="msg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    url: "https://cdn.svgporn.com/logos/vue.svg",
    msg: "Vue.js",
  }),
};
</script>
