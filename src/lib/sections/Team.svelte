<script>
  import Member from "../components/Member.svelte";
  import SectionTitle from "../components/SectionTitle.svelte";
  import { MEMBERS } from "../constants/members";

</script>
<section>
  <SectionTitle>Наша команда</SectionTitle>
  <ul>
    {#each MEMBERS as member}
      <Member {...member} />
    {/each}
  </ul>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 48px;
  }
  ul {
    display: flex;
    gap: 32px 96px;
    flex-wrap: wrap;
  }
</style>
