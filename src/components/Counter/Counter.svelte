<script>
  export let incrementText = '+'
  export let decrementText = '-'
  export let initialValue = 0

  let value = initialValue
  function handleDecClick() {
    value--
  }
  function handleIncClick() {
    value++
  }
</script>

<div class="main-container">
  <div class="button" on:click={handleDecClick}>
    <span>{decrementText}</span>
  </div>
  <div class="value">{value}</div>
  <div class="button" on:click={handleIncClick}>
    <span>{incrementText}</span>
  </div>
</div>

<style>
.main-container {
  display: flex;
  height: 30px;
  user-select: none;
  display: inline-flex;
  border-radius: 5px;
  overflow: hidden;
}
.button {
  width: 50px;
  height: 100%;
  background-color: darkgreen;
  color: white;
  font-size: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
.value {
  width: 50px;
  height: 100%;
  background-color: springgreen;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
}
</style>