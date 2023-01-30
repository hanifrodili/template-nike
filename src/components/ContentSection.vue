<template lang="pug">
.ContentSection
  h1.section-title(v-if="hasTitle")
    slot(name="title")
  slot(name="content")
</template>

<script>
export default {
  name: 'ContentSection',
  computed: {
    hasTitle() {
      return !!this.$slots['title']
    }
  }
}
</script>

<style lang="scss" scoped>
.ContentSection{
  margin-top: 42px;
  padding-bottom: 42px;
  margin-left: 48px;
  margin-right: 48px;
  max-width: 1824px;
  width: auto;

  .section-title{
    font-weight: 500;
    font-size: 24px;
    line-height: 28px;
    margin-bottom: 24px;
  }
}

@media(max-width: 959px) {
  .ContentSection{
     margin-left: 20px;
    margin-right: 20px;
  }
}
</style>
