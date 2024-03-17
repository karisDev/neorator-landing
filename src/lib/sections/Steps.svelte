<script>
  import Chevron from "../components/Chevron.svelte";
  import SectionTitle from "../components/SectionTitle.svelte";
  import Stack from "../components/Stack.svelte";

</script>
<section>
  <SectionTitle white>Как это работает?</SectionTitle>
  <ul>
    <li>
      <span>01</span>
      <div class="card">
        <img src="/assets/mic.svg" alt="микрофон" />
        <span>
          Запишите вступление на диктофон
        </span>
      </div>
    </li>
    <svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M18 36L30 24L18 12" stroke="white" stroke-opacity="0.6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    <li>
      <span>02</span>
      <div class="card">
        <img src="/assets/wand.svg" alt="микрофон" />
        <span>
          Получите аналитику и персональные рекомендации
        </span>
      </div>
    </li>
    <svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M18 36L30 24L18 12" stroke="white" stroke-opacity="0.6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    <li>
      <span>03</span>
      <div class="card">
        <img src="/assets/graph.svg" alt="микрофон" />
        <span>
          Отслеживайте динамику речевых показателей
        </span>
      </div>
    </li>
  </ul>
  <Stack column gap={16} justify="center" align="center">
    <img width="48px" height="48px" src="/assets/rocket.svg" alt="Ракета" />
    <h3>Прокачивайте свою речь!</h3>
  </Stack>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding: 24px;
    margin-top: 60px;
    background-color: var(--primary);
    border-radius: 25px;
  }

  ul {
    display: flex;
    list-style: none;
    width: 100%;
    & :global(.chevron) {
      color: white;
    }
    & > svg {
      margin-block: auto 20px;
    }
  }

  li {
    flex: 1;
    display: flex;
    flex-direction: column;
    & > span:first-child {
      color: white;
      font-size: 3rem;
      font-weight: 200;
      opacity: 0.6;
    }
  }

  .card {
    flex: 1;
    border-radius: 12px;
    background-color: white;
    padding: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  h3 {
    color: #fff;
    font-weight: 500;
    font-size: 1.4rem;
    text-align: center;
  }

  @media (max-width: 850px) {
    section {
      padding: 16px;
    }
    ul {
      flex-direction: column;
    }
    ul > svg {
      margin: 20px auto;
      margin-bottom: 0;
      transform: rotate(90deg);
    }
  }
</style>
