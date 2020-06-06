<template>
  <div id="app">
    <Header />
    <main>
      <section class="left-section">
        <div class="wrap">
          <p class="bread">현재 위치: 블로그 / <span>신규 소식</span></p>
          <div class="headline">
            <h2>신규 소식</h2>
            <ul>
              <li class="on">신규</li>
              <li>추천 게시물</li>
              <li>인기 게시물</li>
            </ul>
          </div>
          <div class="content">
            <div class="content-item" v-for="(e, i) in 6" :key="i">
              <div class="image">이미지</div>
              <div class="information">
                <p class="head"><span>코딩</span><span>2020.06.02</span></p>
                <p class="title">빅데이터 엔지니어 첫걸음<br />데이터 전처리/가공/모델링 개념</p>
                <p class="author"><i>Y</i><span>코딩덕후</span>님 작성</p>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="right-section">
        <div class="wrap">
          <p class="popular">인기게시물</p>
        </div>
      </section>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style lang="scss">
@import '~open-color/open-color.scss';

#app {
  font-family: 'Gothic A1', 'sans-serif';
  font-weight: 400;
  font-size: 14px;
}

main {
  display: flex !important;

  section {
    &.left-section {
      flex-basis: 60%;
      // height: 1000px;
      border-right: 1px solid $oc-gray-1;

      div.wrap {
        width: 700px;
        margin-left: auto;
        margin-right: 30px;

        > p.bread {
          padding: 10px 0;
          border-bottom: 1px solid $oc-gray-1;
          font-size: 12px;
          color: $oc-gray-6;

          > span {
            color: $oc-gray-8;
          }
        }

        div.headline {
          margin-top: 15px;
          margin-bottom: 30px;

          h2 {
            font-weight: 700;
            font-size: 20px;
            color: $oc-gray-8;
          }

          ul {
            float: right;
            vertical-align: top;

            li {
              margin-left: 3px;
              padding: 5px 15px;
              background-color: $oc-gray-4;
              font-weight: 500;
              font-size: 12px;
              color: $oc-white;
              cursor: pointer;

              &.on {
                background-color: $oc-orange-5;
              }
            }
          }
        }

        div.content {
          display: flex;
          flex-wrap: wrap;

          > div.content-item {
            flex-basis: 340px;
            height: 350px;
            margin-bottom: 20px;
            border: 1px solid $oc-gray-1;
            box-sizing: border-box;
            cursor: pointer;

            &:nth-child(even) {
              margin-left: 20px;
            }

            > div.image {
              height: 200px;
              background-color: $oc-blue-5;
            }

            > div.information {
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              height: 150px;
              padding: 20px;
              box-sizing: border-box;

              > p.head {
                // margin-bottom: 15px;

                span {
                  display: inline-block;

                  &:first-child {
                    padding: 2px 15px;
                    border-radius: 10px;
                    background-color: $oc-orange-5;
                    font-weight: 500;
                    font-size: 12px;
                    color: $oc-white;
                  }

                  &:last-child {
                    margin-left: 10px;
                    font-weight: 600;
                    font-size: 11px;
                  }
                }
              }

              > p.title {
                font-weight: 600;
                font-size: 20px;
              }

              > p.author {
                font-weight: 500;
                font-size: 12px;
                color: $oc-gray-5;

                > i {
                  margin-right: 5px;
                  font-style: normal;
                }

                > span {
                  font-weight: 600;
                  color: $oc-gray-8;
                }
              }
            }
          }
        }
      }
    }

    &.right-section {
      flex-basis: 40%;

      div.wrap {
        width: 90%;
        margin: auto;

        > p.popular {
          padding: 10px 0;
          font-weight: 600;
          font-size: 13px;
          border-bottom: 1px solid $oc-gray-1;
          color: $oc-gray-8;
        }
      }
    }
  }
}
</style>
