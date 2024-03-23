<script>
  import FeaturesBg from "../components/FeaturesBg.svelte";
  import SectionTitle from "../components/SectionTitle.svelte";
  import { FEATURES } from "../constants/features";

</script>
<section>
  <FeaturesBg />
  <div class="header">
    <SectionTitle>
      Что под капотом?
    </SectionTitle>
    <p>Мы отслеживаем более 10 речевых показателей</p>
  </div>
  <div class="card left big">
    <img src="/assets/wand.svg" alt="ИИ" />
    <p>ИИ для распознавания речи</p>
  </div>
  <div class="card right big">
    <img src="/assets/timer.svg" alt="ИИ" />
    <p>Обработка аудио длиной до 90 минут</p>
  </div>
  <ul>
    {#each FEATURES as feature}
      <li class="card">
        <img src="/assets/check_ok.svg" alt="Включено" />
        <p>{feature}</p>
      </li>
    {/each}
  </ul>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    margin-top: 20px;
    position: relative;
    width: 100%;
    min-height: 850px;
  }

  ul {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 16px 32px;
    margin-top: 450px;
    margin-inline: auto;
    list-style: none;
    max-width: 650px;
    width: 100%;
  }

  .header {
    display: flex;
    flex-direction: column;
    gap: 16px;
    margin-top: 32px;
    & > * {
      text-align: center;
    }
  }

  .card {
    display: flex;
    align-items: center;
    width: 275px;
    border-radius: 12px;
    border: 1px solid rgba(0, 0, 0, 0.16);
    background: white;
    gap: 0 12px;
    padding: 12px;
    display: grid;
    grid-template-columns: auto 1fr;
    grid-template-rows: 1fr auto;
    grid-template-areas:
      "icon title"
      "icon desc";
    & img {
      grid-area: icon;
    }
    & p {
      grid-area: title;
      font-size: 16px;
      line-height: 24px;
    }
    & span {
      grid-area: desc;
      font-size: 14px;
      color: rgba(0, 0, 0, 0.6);
    }
    &.big {
      padding: 16px;
      & img {
        width: 50px;
        height: 50px;
      }
      &.left {
        position: absolute;
        top: 180px;
        left: calc(max(50px, 10%));
      }
      &.right {
        position: absolute;
        top: 180px;
        right: calc(max(50px, 10%));
      }
    }
  }

  @media (max-width: 768px) {
    .right {
      top: 0;
      right: 0;
    }

    .card.big {
      position: static !important;
      margin-block: 5px;
    }

    .card {
      width: 100%;
    }

    ul {
      margin-top: 10px;
      gap: 16px;
    }
  }
  @media (max-width: 640px) {
    ul {
      gap: 0;
      border-radius: 12px;
      border: 1px solid rgba(0, 0, 0, 0.16);
      overflow: hidden;
      background-color: white;
    }

    ul .card {
      border: none;
      border-radius: 0;
    }
  }
</style>
