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
            Naviguez sur les mers tumultueuses de l’accessibilité numérique et du
            développement web. Hissez les voiles et direction les vastes Terres de
            l’Accessibilité !
          </p>
          <p class="content-header__description">
            Tous à bord du "<span class="content-header__highlight">DevAccess</span
            >", pour des horizons aussi vastes que votre soif d’apprendre. Notre
            périple commence maintenant !
          </p>
        </div>
      </div>
    </header>

    <Seperator />

    <section class="content-section">
      <img src="mapmonde.png" alt="" />
      <div>
        <h2 class="content-section__title">Les chroniques les plus récentes</h2>
        <div class="content-articles">
          <article class="content-article">
            <h3 class="content-article__title">
              Introduction à l’accessibilité
            </h3>
            <p class="content-article__p">
              "Embarquez dans l'exploration de l'accessibilité numérique: un
              trésor d'inclusion pour tous, en particulier les personnes
              handicapées."
            </p>
            <time class="date" datetime="2023-06-25">25 juin 2023</time>
          </article>
          <article>
            <h3>Sensibilisation à l’acessibilité</h3>
            <p>
              "Embarquez dans l'exploration de l'accessibilité numérique: un
              trésor d'inclusion pour tous, en particulier les personnes
              handicapées."
            </p>
            <time class="date" datetime="2023-06-25">25 juin 2023</time>
          </article>
        </div>
        <p class="quote">
          « Naviguer sur le Web sans se soucier de l'accessibilité, c'est comme
          partir en expédition sans emporter de nourriture pour tout l'équipage.
          »
        </p>
      </div>
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
        img {
          margin-inline: auto;
          width: 290px;
          height: auto;
          padding-block: 2rem;
        }
        .content-header__div{
       
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
        img {
          margin-inline: auto;
          width: auto;
          height: 200px;
          padding-block: 1rem 2rem;
        }
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
          border-block: 1px solid #4d4d4d2e;
          padding-block: 2rem;
          @media screen and (min-width: 640px) {
            border: none;
            display: flex;
            gap: 4rem;
          }
          article {
            &:first-child {
              margin-bottom: 2rem;
            }

            h3 {
              @extend %h3-mobile;
              @include h3-mobile;
              @media screen and (min-width: 770px) {
                @include h3-tablet;
              }
              @media screen and (min-width: 1024px) {
                @include h3-desktop;
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
        .quote {
          padding-block: 2rem;
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
