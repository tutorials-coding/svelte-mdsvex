<script>
  export let items = []
</script>
<div class="main-container">
  <div class="header-container">
    {#each items as { title, link }}
      <a target="_blank" href={link}>
        {title}
      </a>
    {/each}
  </div>
  <div class="content-container">
    <slot></slot> 
  </div>
</div>

<style>
.main-container {
  display: flex;
  flex-direction: column;
}
.header-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  height: 200px;
  width: 100%;
  padding: 20px;
  box-sizing: border-box;
  background-color: yellowgreen;
}
.content-container {
  padding: 15px;
}
</style>