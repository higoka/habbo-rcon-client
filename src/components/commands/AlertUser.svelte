<script>
  export const body = {
    key: 'alertuser',
    data: {
      user_id: '',
      message: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" name="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="message">Message</label>
  <textarea name="message" cols="30" rows="5" bind:value={body.data.message}></textarea>
</section>
