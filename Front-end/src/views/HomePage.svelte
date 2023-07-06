<script>
  import Button from "./../components/Button.svelte";
  import { onMount } from "svelte";
  import NavBar from "../components/NavBar.svelte";

  onMount(() => {
    let currentSection = 0;
    const sections = document.querySelectorAll(".scroll-section");
    const navbarHeight = 80;

    window.addEventListener("wheel", (e) => {
      if (e.deltaY > 0) {
        // Scroll vers le bas
        currentSection = Math.min(currentSection + 1, sections.length - 1);
      } else {
        // Scroll vers le haut
        currentSection = Math.max(currentSection - 1, 0);
      }

      window.scrollTo({
        top: sections[currentSection].offsetTop - navbarHeight,
        behavior: "smooth",
      });
    });
  });
</script>

<main class="content-area">
  <div class="content-margin">
    <header class="content-header scroll-section">
      <img src="exploratrice.png" alt="" class="content-header__image" />
      <div class="content-header__div">
        <h1 class="content-header__title">
          L’accessibilité au coeur du développement web
          <hr />
        </h1>
        <div class="content-header__text">
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
        <div class="button">
          <a href="" class="link" aria-label="lien vers la page..."
            >En savoir plus</a
          >
        </div>
      </div>
    </header>

    <section class="content-section scroll-section">
      <div>
        <h2 class="content-section__title">
          Les chroniques les plus récentes
          <hr />
        </h2>
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
        <div class="button">
          <a href="" class="link" aria-label="lien vers la page..."
            >Voir tous les articles</a
          >
        </div>
      </div>
    </section>

    <section class="content-quote scroll-section">
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
    background-color: #f4f8fb9e;
    background-image: url(https://i.ibb.co/DpxkTsx/fond-3.png);
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    background-blend-mode: screen;
    .content-margin {
      margin-inline: 4rem;
      @media screen and (min-width: 640px) {
        margin-inline: 10rem;
      }
      header {
        display: flex;
        flex-direction: column;
        margin-inline: auto;
        max-width: 1091px;

        img {
          margin-inline: auto;
          padding-block: 2rem;
          width: 290px;
          height: auto;
          @media screen and (max-width: 769px) {
            margin-top: 80px;
          }
        }

        .content-header__div {
          h1 {
            @extend %h1-mobile;
            @include h1-mobile;

            hr {
              display: none;
            }
          }

          p {
            @extend %text-mobile;
            @include text-mobile;

            span {
              font-family: $quote-font;
              font-weight: bold;
            }
          }
        }

        .button {
          margin-block: 4rem;
          text-align: center;
          a {
            @extend %button;
          }
        }

        @media screen and (min-width: 770px) {
          display: grid;
          grid-template-rows: auto;
          grid-template-columns: 2fr 1fr;
          padding-block: 2rem;
          align-content: center;

          .content-header__div {
            display: contents;

            h1 {
              grid-row: 1;
              grid-column: 1 / -1;
              @include h1-tablet;

              hr {
                display: block;
                background-color: $color-yellow;
                height: 3px;
                margin-block: 2rem;
                max-width: 425px;
              }
            }

            p {
              @include text-tablet;
            }

            .content-header__description:nth-child(1) {
              grid-row: 2;
              grid-column: 1;
            }

            .content-header__description:nth-child(2) {
              grid-row: 3;
              grid-column: 1;
            }
          }

          img {
            grid-row: 2 / 2;
            grid-column: 2;
            margin-inline: 0;
            padding-block: 0;
            width: auto;
            height: auto;
            justify-self: center;
          }
        }

        @media screen and (min-width: 1024px) {
          .content-header__div {
            h1 {
              @include h1-desktop;
            }
            .content-header__text {
              padding-inline: 5rem;
              p {
                @include text-desktop;
              }
            }
          }
        }

        @media screen and (min-width: 1280px) {
          max-width: 1200px;

          .content-header__div {
            h1 {
              @include h1-desktop-l;
              max-width: 1110px;
            }
            .content-header__text {
              p {
                @include text-desktop-l;
              }
            }
          }
        }

        @media screen and (orientation: landscape) {
          min-height: calc(100dvh - 80px);
          align-items: center;
        }
      }

      section {
        max-width: 1091px;
        @media screen and (min-width: 770px) {
          display: flex;
          justify-content: space-evenly;
          margin-inline: auto;
        }
        @media screen and (min-width: 1280px) {
          max-width: 1200px;
        }

        h2 {
          @extend %h2-mobile;
          margin-top: 5rem;
          @media screen and (min-width: 770px) {
            @include h2-tablet;
          }
          @media screen and (min-width: 1024px) {
            @include h2-desktop;
            margin-bottom: 5rem;
          }
          @media screen and (min-width: 1280px) {
            @include h2-desktop-l;
          }
          hr {
            display: none;
            @media screen and (min-width: 770px) {
              display: block;
              background-color: $color-yellow;
              height: 3px;
              margin-block: 2rem;
              max-width: 425px;
            }
          }
        }
        .content-articles {
          padding-block: 2rem;
          @media screen and (min-width: 640px) {
            display: flex;
            flex-direction: column;
            gap: 2rem;
          }

          @media screen and (min-width: 1024px) {
            display: flex;
            flex-direction: row;
            gap: 4rem;
          }
          .content-article {
            margin-bottom: 2rem;
            background-color: #bfbfbf21;
            border-radius: 12px;
            padding: 4rem 4rem 2rem 4rem;
            box-shadow: 4px 5px 5px #c3c3c3;
            border: 7px solid white;
            background-image: linear-gradient(to top, #f0ebe6 0%, #f5f1ee 100%);
            &:first-child {
              margin-bottom: 2rem;
            }

            h3 {
              display: block;
              @extend %h3-mobile;
              @include h3-mobile;
              @media screen and (min-width: 770px) {
                @include h3-tablet;
              }
              @media screen and (min-width: 1024px) {
                @include h3-desktop;
              }
              @media screen and (min-width: 1280px) {
                @include h3-desktop-l;
              }
              img {
                width: auto;
                height: 30px;
                margin-right: 2rem;
                float: left;
                position: relative;
                @media screen and (min-width: 1024px) {
                  height: 40px;
                }
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
              @media screen and (min-width: 1280px) {
                @include text-desktop-l;
              }
            }

            .date {
              display: flex;
              width: 90%;

              margin-inline: auto;
              margin-top: 2rem;
              @extend %date-mobile;
              @include date-mobile;
              @media screen and (min-width: 640px) {
                @include date-tablet;
                width: 75%;
              }
              @media screen and (min-width: 770px) {
                @include date-tablet;
                width: 65%;
              }
              @media screen and (min-width: 1024px) {
                @include date-desktop;
                width: 75%;
              }
              @media screen and (min-width: 1280px) {
                @include date-desktop-l;
              }
              &::before,
              &::after {
                color: $color-yellow;
                content: "";
                opacity: 50%;
                flex: 1;
                border-bottom: solid 2px;
                margin: auto 1rem;
              }
            }
          }
        }
        .button {
          margin-block: 4rem;
          text-align: center;
          a {
            @extend %button;
          }
        }
      }

      .content-quote {
        @media screen and (min-width: 770px) {
          top: 0;
          margin-top: 80px;
        }
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
          @media screen and (min-width: 1280px) {
            @include quote-desktop-l;
          }
        }
      }
    }
  }
  @media screen and (min-width: 770px) {
    .scroll-section {
      min-height: calc(100vh - 80px);
      position: relative;
      top: 80px;
    }
  }
</style>
