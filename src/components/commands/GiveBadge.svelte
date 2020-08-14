<script>
  export const body = {
    key: 'givebadge',
    data: {
      user_id: '',
      badge: '',
    }
  }
</script>

<section>
  <label for="userId">User Id</label>
  <input type="number" id="userId" min="0" bind:value={body.data.user_id}>
</section>
<section>
  <label for="badge">Badge</label>
  <input type="text" id="badge" bind:value={body.data.badge}>
</section>
