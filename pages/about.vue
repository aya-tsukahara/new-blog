<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle="Example About Page"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>このサイトについて</h3>
          <p>
            ご覧いただきありがとうございます。<br />塚原彩と申します。WEB制作会社で4年ほどコーダーをしています。
          </p>
          <p>
            このサイトは<a
              href="https://github.com/danielkellyio/awake-template"
              target="_blank"
              >Awake</a
            >というテンプレートを使用して制作しています。<br />普段はhtml/css/jQUery/JavaScript/PHPが多いため、Vue.jsとNuxt.jsに触れてみたいと思いこの方法を選びました。<br />全くわからないままカスタマイズをしているので現在Vueの基礎から勉強をしています。
          </p>
          <p>コードを書く上で意識している事<br /></p>
          <dl>
            <div>
              <dt>・メンテナンス性の高いコーディング</dt>
              <dd>
                CSS→再利用可能なCSS設計を目指しています。classはFLOCSSを使っています
              </dd>
              <dd>
                html→普段はejsを使用して繰り返しのデザインはオブジェクトなどにまとめてコーディングしています
              </dd>
            </div>
            <div>
              <dt>・自分なりの工夫をする事</dt>
              <dd>
                基本的に複数の案件を抱えています。実コーディング時間が取れない中でも、「もっとこうしたら使いやすくなるのでは」を考え<br />
                実装の検証〜ご提案をするようにしています。
              </dd>
            </div>
          </dl>
          <!-- <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit!
          </p>

          <h3>Another Fake Heading</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit!
          </p>
          <quote-card />
          <h3>Still More Fake Content</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit.
            <strong>Alias aut facere harum ipsam</strong> quibusdam quidem
            quisquam saepe? Alias architecto blanditiis consequatur consequuntur
            dicta ipsa iste modi provident, quod, similique veritatis.
          </p> -->
        </div>

        <!-- <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div> -->
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  }
  // components: { QuoteCard }
}
</script>
