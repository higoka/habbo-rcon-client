<script>
  export const body = {
    key: 'givepixels',
    data: {
      user_id: '',
      pixels: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" id="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="amount">Amount</label>
  <input type="number" id="amount" bind:value={body.data.pixels}>
</section>
