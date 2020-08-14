<script>
  export const body = {
    key: 'disconnect',
    data: {
      user_id: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" name="userId" min="0" bind:value={body.data.user_id}>
</section>
