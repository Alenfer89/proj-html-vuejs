<template>
  <div class="ax-carousel-element me-5 mb-5 mt-1 d-inline-block shadow">
    <div class="img-wrapper">
      <img :src="require(`../assets/images/${thumbnail}`)" :alt="name" />
    </div>
    <div class="d-flex justify-content-between">
      <h6 class="ax-bold p-2">{{ name }}</h6>
      <p class="m-0 p-2">{{ category }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CarouselCard",
  props: {
    name: String,
    category: String,
    thumbnail: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/style.scss";
div.ax-carousel-element {
  width: calc((100% / 5));
  //   width: 5rem;
  white-space: normal;
  border-radius: 2rem;

  &:hover {
    color: white;
    cursor: pointer;
    @include bgGradientLeftToRight($secondaryColor, $secondaryLightColor);
  }

  div.img-wrapper {
    border-radius: 2rem;
    width: 100%;
    img {
      width: 100%;
      border-radius: 2rem;
    }
  }
}

// @media screen and (max-width: 900px) {
//   div.ax-carousel-element {
//     width: calc((100% / 2) + 100px);
//   }
// }

// @media screen and (max-width: 600) {
//   div.ax-carousel-element {
//     width: 100%;
//   }
// }
</style>
