<script>
  import Hero from "./lib/sections/Hero.svelte";
  import Steps from "./lib/sections/Steps.svelte";
  import Features from "./lib/sections/Features.svelte";
  import Team from "./lib/sections/Team.svelte";
  import Footer from "./lib/sections/Footer.svelte";

</script>

<main class="section">
  <Hero />
  <Steps />
  <Features />
  <img src="/assets/histogram.webp" alt="Звуковая волна" />
  <Team />
</main>
<Footer />

<style>
  .section {
    max-width: var(--content-width);
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    flex-direction: column;
  }

  img {
    margin-block: 64px;
    object-fit: cover;
    min-height: 64px;
  }
</style>
