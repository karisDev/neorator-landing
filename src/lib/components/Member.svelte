<script>
  export let name = "";
  export let description = "";
</script>

<li>
  <img src={$$props.imgSrc} alt="Фото участника команды: {name}" />
  <div>
    <p>{name}</p>
    <p>{description}</p>
  </div>
</li>

<style>
  li {
    display: flex;
    gap: 0 24px;
    flex: 1;
  }

  img {
    width: 96px;
    height: 96px;
    border-radius: 50%;
  }

  p:nth-child(1) {
    grid-area: name;
    font-weight: 500;
    font-size: 1.25rem;
  }

  p:nth-child(2) {
    grid-area: description;
    text-wrap: pretty;
    min-width: 240px;
    max-width: 420px;
    font-size: 1rem;
  }
  
  @media screen and (max-width: 500px) {
    p:nth-child(3) {
      min-width: 0;
    }
  }
</style>
