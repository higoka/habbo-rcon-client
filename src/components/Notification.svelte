<script>
  import { fly } from 'svelte/transition'

  export let error = false
  export let result

  setTimeout(() => result = false, 3000)
</script>

<p class={error ? 'error' : 'success'} transition:fly={{ x: 200, duration: 500 }}>
  <slot />
</p>

<style>
  p {
    padding: 16px;
    right: 24px;
    top: 24px;
    margin: 0;
    border-radius: 4px;
    color: #fff;
    position: fixed;
  }

  .error {
    background-color: #ff4757;
  }

  .success {
    background-color: #2ed573;
  }
</style>
