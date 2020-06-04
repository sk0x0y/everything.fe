<template>
  <div id="app">
    <header>
      <h1 class="brand">에브리띵</h1>
      <ul class="menu">
        <li><router-link to="/">공지사항</router-link></li>
        <li><router-link to="/">자유게시판</router-link></li>
        <li><router-link to="/">고객센터</router-link></li>
      </ul>
      <div class="search-form">
        <input type="text" placeholder="검색어를 입력해주세요" />
        <button type="button">검색</button>
      </div>
      <ul class="member">
        <li><router-link to="/">기존회원</router-link></li>
        <li><router-link to="/">신규회원</router-link></li>
      </ul>
    </header>
    <main>
      <section class="left-section">
        <div class="wrap">
          <nav>현재 위치: 블로그 / 신규 소식</nav>
        </div>
      </section>
      <section class="right-section">
        <div class="wrap">safsd</div>
      </section>
    </main>
    <footer>
      <h1 class="brand">에브리띵</h1>
      <p>Copyright &copy; 에브리띵, All Rights Reserved.</p>
      <p>커뮤니티에 올라온 게시물의 모든 책임은 게시물 작성자에게 있습니다.</p>
    </footer>
  </div>
</template>

<style lang="scss">
@import '~open-color/open-color.scss';

#app {
  font-family: 'Gothic A1', 'sans-serif';
  font-weight: 400;
  font-size: 14px;
}

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
    }
  }

  div.search-form {
    margin-left: 30px;

    input {
      width: 200px;
    }
  }

  ul.member {
    margin: 0 30px;

    li {
      margin-left: 10px;
    }
  }
}

main {
  display: flex !important;

  section {
    &.left-section {
      flex-basis: 60%;
      height: 1000px;
      border-right: 1px solid $oc-gray-1;

      div.wrap {
        width: 700px;
        margin-left: auto;
        margin-right: 30px;
      }
    }

    &.right-section {
      flex-basis: 40%;
    }

    nav {
      border-bottom: 1px solid $oc-gray-1;
    }
  }
}

footer {
}
</style>
