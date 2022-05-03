<template>
  <div
    class="new px-6 px-md-10 py-16 mx-7 mb-8"
    style="position: relative"
    :style="
      $vuetify.breakpoint.lgAndUp
        ? 'width:350px; height:400px'
        : $vuetify.breakpoint.mdAndUp
        ? 'width:250px; min-height:300px;max-height:500px'
        : 'max-width:90%; min-height:250px;max-height:450px'
    "
  >
    <div
      :style="
        $vuetify.breakpoint.lgAndUp ? 'font-size: 18px' : 'font-size: 18px'
      "
      v-html="
        $vuetify.breakpoint.name == 'xl'
          ? post.title.slice(0, 80) + '...'
          : $vuetify.breakpoint.name == 'lg'
          ? post.title.slice(0, 70) + '...'
          : $vuetify.breakpoint.name == 'sm'
          ? post.title.slice(0, 70) + '...'
          : $vuetify.breakpoint.name == 'xs'
          ? post.title.slice(0, 70) + '...'
          : post.title.slice(0, 70) + '...'
      "
      class="new--title"
    ></div>
    <div
      :style="
        $vuetify.breakpoint.lgAndUp ? 'font-size: 14px' : 'font-size: 14px'
      "
      class="mt-4 new--description"
      v-html="
        $vuetify.breakpoint.name == 'xl'
          ? post.description.slice(0, 140) + '...'
          : $vuetify.breakpoint.name == 'lg'
          ? post.description.slice(0, 120) + '...'
          : $vuetify.breakpoint.name == 'sm'
          ? post.description.slice(0, 150) + '...'
          : $vuetify.breakpoint.name == 'xs'
          ? post.description.slice(0, 150) + '...'
          : post.description.slice(0, 70) + '...'
      "
    ></div>
    <v-btn
      style="
        position: absolute;
        bottom: 10px;
        left: 50%;
        transform: translateX(-50%);
      "
      color="green"
      text
      outlined
      :href="post.link"
      target="_blank"
      >Подробнее</v-btn
    >
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" >
.new {
  -webkit-box-shadow: 0px 0px 11px 4px rgba(5, 6, 5, 0.2);
  -moz-box-shadow: 0px 0px 11px 4px rgba(5, 6, 5, 0.2);
  box-shadow: 0px 0px 11px 4px rgba(5, 6, 5, 0.2);
  &--title {
    font-weight: 700;
  }
  &--description {
    font-weight: 300;
  }
}
</style>