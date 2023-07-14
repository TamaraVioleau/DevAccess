<script>
</script>

<main class="content-area">
  <div class="content-margin">
    <header class="content-header scroll-section">
      <img src="woman-desk.png" alt="" class="content-header__image" />
      <div class="content-header__div">
        <h1 class="content-header__title">
          Derrière l'écran se cache ...
          <hr />
        </h1>
        <div class="content-header__text">
          <h2 class="content-header__h2 description-color">
            Tamara, développeuse front-end formée à l'accessibilité numérique.
          </h2>
          <p class="content-header__description">
            <!-- <span class="content-header__highlight"></span> -->
            Je suis une passionnée de l'accessibilité numérique. En tant qu'introvertie
            empathique et hypersensible, j'ai toujours été touchée par les inégalités.
            A l'époque, je manquais de courage pour me battre pour mes idéaux. Aujourd'hui,
            je m'investis pour une cause qui me tient à cœur : rendre le numérique
            accessible à tous.
          </p>
          <h2 class="content-header__h2 description-color">Mon parcours</h2>
          <p class="content-header__description">
            <!-- <span class="content-header__highlight"></span> -->
            Mon parcours a été pour le moins diversifié et riche en apprentissages.
            J'ai commencé avec un BAFA spécialisé dans l'accompagnement des enfants
            handicapés, dix d'animation en colonie de vacances, parfois aux côtés
            d'enfants en situation de handicap. Ces expériences m'ont ouvert les
            yeux sur la complexité du monde vu à travers les yeux des personnes handicapées,
            et ont laissé en moi une empreinte indélébile.
          </p>
          <p class="content-header__description">
            Ma carrière m'a ensuite menée vers le domaine de la petite enfance.
            J'ai décroché mon diplôme d'éducatrice de jeunes enfants et j'ai
            travaillé pendant une année en école Montessori, suivie de deux
            années en crèche. Mes expériences m'ont permises de me former sur le
            terrain, de travailler de près avec les enfants présentant des
            handicaps, et d'adapter mes méthodes en fonction de leurs forces et
            de leurs faiblesses.
          </p>
          <p class="content-header__description">
            Ce n'est qu'après ces années enrichissantes que j'ai opéré un virage
            surprenant vers le développement web. Pourquoi ? Car je souhaitais
            voulait faire de ma passion pour le développement web mon univers
            professionnel.
          </p>

          <h2 class="content-header__h2 description-color">
            L'éveil de ma conscience numérique
          </h2>
          <p class="content-header__description">
            Ma transition vers le développement web n'a fait que renforcer mon
            engagement pour l'accessibilité numérique. Lors de ma formation en
            développement web, j'ai été initiée à l'accessibilité numérique.
            J'avais déjà une certaine conscience de l'importance de cette cause
            grâce à ma passion pour les jeux de rôle sur forums, où les
            discussions sur l'apparence des sites (taille et style de police,
            contraste, lisibilité) étaient courantes. Cependant, ma formation a
            approfondi ma compréhension de l'accessibilité numérique et m'a fait
            réaliser l'ampleur de la tâche à accomplir.
          </p>

          <p class="content-header__description">
            Un stage de six mois aux côtés d'un développeur aveugle spécialisé
            dans l'accessibilité a fini de me convaincre : ce serait ma cause,
            mon engagement. Ces mois passés à ses côtés m'ont beaucoup appris et
            ont été l'impulsion qui m'a menée à la création de ce blog.
          </p>

          <p class="content-header__description">
            Je suis là aujourd'hui, prête à partager avec vous ce que j'ai
            appris, et ce que nous avons encore à apprendre ensemble. Car
            l'accessibilité numérique, ce n'est pas seulement rendre le web
            utilisable pour tous, c'est aussi reconnaître que nous avons tous un
            rôle à jouer pour que le numérique soit une chance pour tous, et non
            une barrière.
          </p>
        </div>
        <div class="button">
          <a href="/" class="link" aria-label="lien vers la page..."
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
              <a href="/">Introduction à l’accessibilité</a>
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
          <a href="/" class="link" aria-label="lien vers la page..."
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
    @extend %main;
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
        }

        .content-header__div {
          h1 {
            @extend %h1-mobile;
            @include h1-mobile;
            text-align: center;

            hr {
              display: block;
                background-color: $color-yellow;
                height: 3px;
                margin-block: 2rem;
                max-width: 425px;
                margin-inline: auto;
                width: 50%;
            }
          }

          .content-header__text {
            background: #ffffff7a;
            padding: 2rem;
            margin-inline: 2rem;
            border-radius: 1rem;
            p {
              @extend %text-mobile;
              @include text-mobile;

              span {
                font-family: $quote-font;
                font-weight: bold;
              }
            }
            .description-color {
              color: $title-color;
              font-weight: bold;
            }
            h2 {
              @extend %h2-mobile;
            }
          }
        }

        .button {
          margin-block: 4rem;
          text-align: center;
          a {
            @extend %button;
            transition: background-color 0.3s, color 0.3s;
          }
        }

        @media screen and (min-width: 770px) {
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
                margin-inline: auto;
                width: 75%;
              }
            }
            h2 {
              @include h2-tablet;
            }
            p {
              @include text-tablet;
            }
          }

          img {
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
              h2 {
                @include h2-desktop;
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

      .content-section {
        max-width: 1091px;
        align-items: center;
        @media screen and (min-width: 770px) {
          display: flex;
          justify-content: space-evenly;
          margin-inline: auto;
        }
        @media screen and (min-width: 1280px) {
          max-width: 1200px;
        }

        @media screen and (orientation: landscape) {
          min-height: calc(100dvh - 80px);
          align-items: center;
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

              a {
                @extend %link;
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
            transition: background-color 0.3s, color 0.3s;
          }
        }
      }

      .content-quote {
        @media screen and (min-width: 770px) {
        }

        @media screen and (orientation: landscape) {
          min-height: calc(100dvh - 80px);
          align-items: center;
          display: flex;
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
</style>
