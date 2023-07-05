<script>
  import { onMount } from 'svelte';

  onMount(() => {
    let currentSection = 0;
    const sections = document.querySelectorAll('.section');
    const navbarHeight = 80;

    window.addEventListener('wheel', (e) => {
      if (e.deltaY > 0) {
        // Scroll vers le bas
        currentSection = Math.min(currentSection + 1, sections.length - 1);
      } else {
        // Scroll vers le haut
        currentSection = Math.max(currentSection - 1, 0);
      }

      window.scrollTo({
        top: sections[currentSection].offsetTop - navbarHeight,
        behavior: 'smooth',
      });
    });
  });
</script>

<style>
  .section {
    min-height: calc(100vh - 80px);
    position: relative;
    top: 80px;
  }

  .section1 {
    background-color: #f00;
  }

  .section2 {
    background-color: #0f0;
  }

  .section3 {
    background-color: #00f;
  }
</style>


<div class="section section1" id="section1">Section 1</div>
<div class="section section2" id="section2">Section 2</div>
<div class="section section3" id="section3">Section 3</div>
