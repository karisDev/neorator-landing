<footer>
  <div class="content">
    <a href="#hero">
      <img src="/favicon.svg" alt="Не оратор" />
      <span>NeOrator</span>
    </a>
    <a href="https://disk.yandex.ru/d/rF1hIvXO-cEzAA/">Скачать презентацию</a>
    <a href="mailto:ipleshakov4@gmail.com">ipleshakov4@gmail.com</a>
  </div>
</footer>

<style>
  footer {
    margin-top: 120px;
    background: var(--primary);
    padding-block: 32px;
  }

  .content {
    max-width: var(--content-width);
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    align-items: center;
    gap: 48px;
  }

  img {
      width: 64px;
  }

  a {
    color: white;
    text-decoration: none;
    cursor: pointer;
  }

  a:first-child {
    display: flex;
    align-items: center;
    gap: 12px;
    & span {
      font-size: 1.25rem;
      font-weight: 600;
    }
  }

  a:last-child {
    margin-left: auto;
  }

  @media screen and (max-width: 700px) {
    .content {
      flex-direction: column;
      gap: 24px;
    }

    img {
      width: 48px;
    }

    a:last-child {
      margin-left: 0;
    }
  }
</style>
