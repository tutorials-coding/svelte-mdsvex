<script context="module"> 
  import Table from './custom/Table.svelte'
  import Th from './custom/Th.svelte'
  import Tr from './custom/Tr.svelte'
  import Td from './custom/Td.svelte'

  export {
    Table as table,
    Th as th,
    Tr as tr,
    Td as td
  }
</script>

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