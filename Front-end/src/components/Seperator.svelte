<script>
</script>

<div class="icon">
  <img src="protect.png" />
</div>

<style lang="scss">
  @import "../styles/extends";
  @import "../styles/mixins";
  @import "../styles/variables";

  .icon {
    display: flex;
    font-family: $text-font;
    color: $text-color;
    font-size: 1.2rem;
    margin-inline: auto;
    height: 30px;
    width: 90%;

    @media screen and (min-width: 770px) {
      height: 45px;
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
</style>
