<script>
  export const body = {
    key: 'staffalert',
    data: {
      message: '',
    }
  }
</script>

<section>
  <label for="message">Message</label>
  <textarea name="message" cols="30" rows="5" bind:value={body.data.message}></textarea>
</section>
