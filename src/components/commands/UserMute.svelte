<script>
  export const body = {
    key: 'muteuser',
    data: {
      user_id: '',
      duration: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" id="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="duration">Duration (milliseconds)</label>
  <input type="number" id="duration" min="0" bind:value={body.data.duration}>
</section>
