<template>
  <footer>
    <h1 class="brand">에브리띵</h1>
    <p>Copyright &copy; 에브리띵, All Rights Reserved.</p>
    <p>커뮤니티에 올라온 게시물의 모든 책임은 게시물 작성자에게 있습니다.</p>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped lang="scss">
@import '~open-color/open-color.scss';

footer {
  padding: 50px 0;
  border-top: 1px solid $oc-gray-1;
  font-size: 13px;
  color: $oc-gray-7;
  text-align: center;

  > * {
    padding: 5px 0;
  }
}
</style>
