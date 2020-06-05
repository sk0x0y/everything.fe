<template>
  <header>
    <h1 class="brand">에브리띵</h1>
    <ul class="menu">
      <li><router-link to="/">공지사항</router-link></li>
      <li><router-link to="/">자유게시판</router-link></li>
      <li><router-link to="/">고객센터</router-link></li>
    </ul>
    <div class="search-form">
      <input type="text" placeholder="검색어를 입력해주세요" />
      <button type="button" />
    </div>
    <ul class="member">
      <li class="exist"><router-link to="/">기존회원</router-link></li>
      <li class="new"><router-link to="/">신규회원</router-link></li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped lang="scss">
@import '~open-color/open-color.scss';

header {
  display: flex;
  height: 70px;
  line-height: 70px;
  text-align: center;
  border-bottom: 1px solid $oc-gray-2;

  h1.brand {
    margin-left: 60px;
  }

  ul.menu {
    margin: 0 0 0 auto;

    li {
      margin-left: 20px;
      font-weight: 700;
    }
  }

  div.search-form {
    margin-left: 30px;
    border-left: 1px solid $oc-gray-1;
    border-right: 1px solid $oc-gray-1;

    input {
      width: 400px;
      height: 100%;
      padding: 0 20px;
      border: none;
      box-sizing: border-box;

      &::placeholder {
        color: $oc-gray-5;
      }
    }

    button {
      width: 30px;
      height: 30px;
      margin-right: 20px;
      border: none;
      background-image: url('../assets/search.png');
      background-position: center center;
      background-size: contain;
      background-repeat: no-repeat;
      background-color: transparent;
      appearance: none;
      vertical-align: middle;
      cursor: pointer;
    }
  }

  ul.member {
    margin: 0 30px;

    li {
      margin-left: 10px;
      padding: 3px 7px;
      border-radius: 2px;
      font-weight: 600;
      line-height: normal;

      &.new {
        background-color: $oc-orange-5;

        a {
          color: $oc-white;
        }
      }
    }
  }
}
</style>
