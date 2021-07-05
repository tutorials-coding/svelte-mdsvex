<script>
  export let subtitle = ''
</script>
<div class="main-container">
  <div class="header-container">
    <h1>Counter</h1>
    <h2>{subtitle}</h2>
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
  align-items: center;
  justify-content: center;
  height: 200px;
  width: 100%;
  background-color: yellowgreen;
}
.content-container {
  padding: 15px;
}
</style>