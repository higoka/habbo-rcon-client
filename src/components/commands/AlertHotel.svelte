<script>
  export const body = {
    key: 'hotelalert',
    data: {
      message: '',
      url: '',
    }
  }
</script>

<section>
  <label for="message">Message</label>
  <textarea name="message" cols="30" rows="5" bind:value={body.data.message}></textarea>
</section>
<section>
  <label for="url">URL (optional)</label>
  <input type="text" id="url" bind:value={body.data.url}>
</section>
