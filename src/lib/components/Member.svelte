<script>
  export let name = "";
  export let description = "";
</script>

<li>
  <img src={$$props.imgSrc} alt="Фото участника команды: {name}" />
  <p>{name}</p>
  <p>{description}</p>
</li>

<style>
  li {
    display: grid;
    grid-template-columns: auto 1fr;
    grid-template-rows: auto auto;
    grid-template-areas:
      "img name"
      "img description";
    gap: 0 24px;
    flex: 1;
  }

  img {
    grid-area: img;
    width: 96px;
    height: 96px;
    border-radius: 50%;
  }

  p:nth-child(2) {
    grid-area: name;
    font-weight: 500;
    font-size: 1.25rem;
  }

  p:nth-child(3) {
    grid-area: description;
    text-wrap: pretty;
    min-width: 312px;
    max-width: 420px;
    font-size: 1rem;
  }
  
  @media screen and (max-width: 500px) {
    p:nth-child(3) {
      min-width: 0;
    }
  }
</style>
