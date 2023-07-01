<script>
  import Seperator from "../components/Seperator.svelte";
</script>

<main class="content-area">
  <div class="content-margin">
    <header class="content-header">
      <img src="exploratrice.png" alt="" />
      <div class="content-header__div">
        <h1 class="content-header__title">
          L’accessibilité au coeur du développement web
        </h1>
        <div>
          <p class="content-header__description">
            Naviguez sur les mers tumultueuses de l’accessibilité numérique et
            du développement web. Hissez les voiles et direction les vastes
            Terres de l’Accessibilité !
          </p>
          <p class="content-header__description">
            Tous à bord du "<span class="content-header__highlight"
              >DevAccess</span
            >", pour des horizons aussi vastes que votre soif d’apprendre. Notre
            périple commence maintenant !
          </p>
        </div>
      </div>
    </header>

    <section class="content-section">
      <div>
        <h2 class="content-section__title">Les chroniques les plus récentes</h2>
        <div class="content-articles">
          <article class="content-article">
            <h3 class="content-article__title">
              <img src="/punaises.png" alt="" />

              Introduction à l’accessibilité
            </h3>
            <p class="content-article__p">
              "Embarquez dans l'exploration de l'accessibilité numérique: un
              trésor d'inclusion pour tous, en particulier les personnes
              handicapées."

              <time class="date" datetime="2023-06-25">25 juin 2023</time>
            </p>
          </article>
          <article class="content-article">
            <h3 class="content-article__title">
              <img src="/punaises.png" alt="" />

              Introduction à l’accessibilité
            </h3>
            <p class="content-article__p">
              "Embarquez dans l'exploration de l'accessibilité numérique: un
              trésor d'inclusion pour tous, en particulier les personnes
              handicapées."

              <time class="date" datetime="2023-06-25">25 juin 2023</time>
            </p>
          </article>
        </div>
      </div>
    </section>

    <section class="content-quote">
      <p class="quote">
        « Naviguer sur le Web sans se soucier de l'accessibilité, c'est comme
        partir en expédition sans emporter de nourriture pour tout l'équipage. »
      </p>
    </section>
  </div>
</main>

<style lang="scss">
  @import "../styles/extends";
  @import "../styles/mixins";
  @import "../styles/variables";

  main {
    min-height: 100vh;
    background-color: $bg-color;
    .content-margin {
      margin-inline: 4rem;
      header {
        display: flex;
        flex-direction: column;
        margin-inline: auto;
        max-width: 1091px;
        @media screen and (min-width: 770px) {
          flex-direction: row-reverse;
          padding-block: 2rem;
          justify-content: space-evenly;
        }
        @media screen and (orientation: landscape) {
          min-height: calc(100dvh - 80px);
          display: flex;
          align-items: center;
        }
        img {
          margin-inline: auto;
          padding-block: 2rem;
          width: 290px;
          height: auto;

          @media screen and (min-width: 770px) {
            margin-inline: 0;
            padding-block: 0;
            width: auto;
            height: 100%;
            max-height: 295px;
            align-self: center;
          }
        }
        .content-header__div {
          @media screen and (min-width: 770px) {
            max-width: 740px;
          }

          h1 {
            @extend %h1-mobile;
            @include h1-mobile;
            @media screen and (min-width: 770px) {
              @include h1-tablet;
            }
            @media screen and (min-width: 1024px) {
              @include h1-desktop;
            }
          }

          p {
            @extend %text-mobile;
            @include text-mobile;
            @media screen and (min-width: 770px) {
              @include text-tablet;
            }
            @media screen and (min-width: 1024px) {
              @include text-desktop;
            }

            span {
              font-family: $quote-font;
              font-weight: bold;
            }
          }
        }
      }

      section {
        max-width: 1091px;
        @media screen and (min-width: 770px) {
          display: flex;
          justify-content: space-evenly;
          margin-inline: auto;
        }
        // @media screen and (orientation: landscape) {
        //   min-height: calc(100dvh - 80px);
        //   display: flex;
        //   align-items: center;
        // }
        h2 {
          @extend %h1-mobile;
          @media screen and (min-width: 770px) {
            @include h1-tablet;
          }
          @media screen and (min-width: 1024px) {
            @include h1-desktop;
          }
        }
        .content-articles {
          padding-block: 2rem;
          @media screen and (min-width: 640px) {
            display: flex;
            gap: 4rem;
          }
          article {
            max-width: 560px;
            margin-bottom: 2rem;
            background-color: #fffcf5;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 4px 5px 5px #c3c3c3;
            &:first-child {
              margin-bottom: 2rem;
            }

            h3 {
              display: flex;
              @extend %h3-mobile;
              @include h3-mobile;
              @media screen and (min-width: 770px) {
                @include h3-tablet;
              }
              @media screen and (min-width: 1024px) {
                @include h3-desktop;
              }
              img {
                width: auto;
                height: 45px;
                margin-right: 2rem;
              }
            }

            p {
              @extend %text-mobile;
              @include text-mobile;
              @media screen and (min-width: 770px) {
                @include text-tablet;
              }
              @media screen and (min-width: 1024px) {
                @include text-desktop;
              }
            }

            .date {
              display: flex;
              width: 90%;
              margin-inline: auto;
              margin-top: 2rem;
              @extend %date-mobile;
              @include date-mobile;
              @media screen and (min-width: 770px) {
                @include date-tablet;
              }
              @media screen and (min-width: 1024px) {
                @include date-desktop;
              }

              &::before,
              &::after {
                color: $text-color;
                content: "";
                flex: 1;
                border-bottom: solid 2px;
                margin: auto 1rem;
              }
            }
          }
        }
      }

      .content-quote {
        .quote {
          padding-block: 2rem;
          border: 2px solid #d9ae46;
          padding: 10rem 5rem;
          @extend %quote-mobile;
          @include quote-mobile;
          @media screen and (min-width: 770px) {
            @include quote-tablet;
          }
          @media screen and (min-width: 1024px) {
            @include quote-desktop;
          }
        }
      }
    }
  }
</style>
