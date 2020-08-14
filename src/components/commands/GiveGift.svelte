<script>
  export const body = {
    key: 'sendgift',
    data: {
      user_id: '',
      itemid: '',
      message: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" id="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="itemId">Item Id</label>
  <input type="number" id="itemId" min="0" bind:value={body.data.itemid}>
</section>
<section>
  <label for="message">Message (optional)</label>
  <textarea name="message" cols="30" rows="5" bind:value={body.data.message}></textarea>
</section>
