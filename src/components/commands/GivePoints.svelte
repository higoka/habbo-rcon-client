<script>
  export const body = {
    key: 'givepoints',
    data: {
      user_id: '',
      type: '',
      points: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" id="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="type">Type</label>
  <input type="number" id="type" min="0" bind:value={body.data.type}>
</section>
<section>
  <label for="amount">Amount</label>
  <input type="number" id="amount" bind:value={body.data.points}>
</section>
