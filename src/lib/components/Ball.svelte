<script>
  export let colors = ["#9cc5a1", "#49a078", "#216869", "#1f2421"];

  const getRandomColor = () => {
    const randomIndex = Math.floor(Math.random() * colors.length);
    return colors[randomIndex];
  };
</script>

<div
  class="ball"
  style="
    --color: {getRandomColor()};
  "
></div>

<style>
  .ball {
    border-radius: 50%;
    display: inline-block;
    background-color: var(--color);
    width: 18px; /* Default size */
    height: 18px; /* Default size */
  }

  /* Media query for screens with a max width of 768px */
  @media (max-width: 768px) {
    .ball {
      width: 12px; /* Size for mobile devices */
      height: 12px; /* Size for mobile devices */
    }
  }
</style>
