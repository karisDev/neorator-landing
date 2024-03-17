<div class="wrapper" aria-hidden="true">
  <div class="container">
    <img class="center-logo" src="/assets/logo.svg" alt="Логотип Не Оратор" />
    {#each Array(5) as _, i}
      <span style="--size: {250 + i * 150}px; opacity: {1 - i * 0.2};"
            class="ring" />
    {/each}
  </div>
</div>

<style>
  .wrapper {
    position: absolute;
    width: 100%;
    pointer-events: none;
  }

  .container {
    position: relative;
    height: 850px;
  }

  .ring {
    position: absolute;
    border-radius: 50%;
    z-index: -1;
    border: 1px solid var(--primary);
    width: var(--size);
    height: var(--size);
    top: calc(850px / 2 - var(--size) / 2);
    left: calc(100% / 2 - var(--size) / 2);
  }

  .center-logo {
    position: absolute;
    top: calc(850px / 2 - 100px / 2);
    left: 50%;
    transform: translateX(-50%);
    z-index: -1;
  }

  @media (max-width: 768px) {
    img {
      opacity: 0.4;
      filter: grayscale(1);
    }
  }
</style>
