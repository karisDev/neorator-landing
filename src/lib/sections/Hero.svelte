<script>
  import Chevron from "../components/Chevron.svelte";
  import Stack from "../components/Stack.svelte";

</script>

<section id="hero">
  <img class="mobile-logo" src="/favicon.svg" alt="Логотип" />
  <Stack column class="content">
    <h1>NеOrator</h1>
    <p>Надежный помощник в сфере совершенствования речевых навыков</p>
  </Stack>
  <Stack align="center" gap={12} wrap>
    <a class="primary" target="_blank" href="https://disk.yandex.ru/d/rF1hIvXO-cEzAA/">
      <img src="/assets/download.svg" width="20px" height="20px" alt="Скачать: " />
      Презентация для инвесторов
    </a>
    <a class="transparent" target="_blank" href="mailto:ipleshakov4@gmail.com">Связаться <Chevron direction="right" size={20} /></a>
  </Stack>
  <img class="shadow-img" src="/favicon.svg" alt="" />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 32px;
    padding-top: 150px;
    position: relative;
  }

  .mobile-logo {
    width: 100px;
    height: 100px;
    display: none;
  }

  .shadow-img {
    position: absolute;
    right: 0%;
    top: 60%;
    width: 30%;
    height: 70%;
    transform: translateY(-50%);
    z-index: -1;
  }
  
  @media screen and (max-width: 910px) {
    .shadow-img {
      display: none;
    }
    .mobile-logo {
      display: block;
    }
  }

  h1 {
    color: var(--primary);
  }

  p {
    max-width: 728px;
    text-wrap: pretty;
  }

  a {
    text-decoration: none;
    border-radius: 12px;
    display: flex;
    align-items: center;
    padding: 12px 16px;
    gap: 8px;
    font-size: 1rem;
    line-height: 1.4;
    text-align: start;
    transition: background-color 0.2s;
  }

  .primary {
    background-color: var(--primary);
    color: white;
    &:hover {
      background-color: var(--primary-hover);
    }
  }

  .transparent {
    color: #191919;
    border-radius: 12px;
    &:hover {
      background-color: #f5f5f5;
    }
  }
</style>
