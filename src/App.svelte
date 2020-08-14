<script>
  import Notification from './components/Notification.svelte'

  import AlertHotel from './components/commands/AlertHotel.svelte'
  import AlertStaff from './components/commands/AlertStaff.svelte'
  import AlertUser from './components/commands/AlertUser.svelte'
  import GiveCredits from './components/commands/GiveCredits.svelte'
  import GivePixels from './components/commands/GivePixels.svelte'
  import GiveDiamonds from './components/commands/GiveDiamonds.svelte'
  import GivePoints from './components/commands/GivePoints.svelte'
  import GiveBadge from './components/commands/GiveBadge.svelte'
  import GiveGift from './components/commands/GiveGift.svelte'
  import UserMute from './components/commands/UserMute.svelte'
  import UserDisconnect from './components/commands/UserDisconnect.svelte'
  import UpdateCatalog from './components/commands/UpdateCatalog.svelte'
  import UpdateWordfilter from './components/commands/UpdateWordfilter.svelte'

  const commands = [
    { component: AlertHotel, description: 'Send message to all users' },
    { component: AlertStaff, description: 'Send message to all staffs' },
    { component: AlertUser, description: 'Send message to user' },
    { component: GiveCredits, description: 'Give user credits' },
    { component: GivePixels, description: 'Give user duckets' },
    { component: GiveDiamonds, description: 'Give user diamonds' },
    { component: GivePoints, description: 'Give user points' },
    { component: GiveBadge, description: 'Give user badges' },
    { component: GiveGift, description: 'Give user gifts' },
    { component: UserMute, description: 'Mute user' },
    { component: UserDisconnect, description: 'Disconnect user' },
    { component: UpdateWordfilter, description: 'Update the catalog' },
    { component: UpdateCatalog, description: 'Update the wordfilter' },
  ]

  let component
  let body
  let result = false

  async function handleSubmit () {
    try {
      const res = await fetch(API_HOST, { method: 'POST', body: JSON.stringify(body) })
      result = await res.json()
    } catch (err) {
      result = { error: true, message: err.message }
    }
  }
</script>

{#if result}
  <Notification error={result.error} bind:result>
    {result.message}
  </Notification>
{/if}
<main>
  <img src="img/morningstar.png" alt="Morningstar Logo">
  <form on:submit|preventDefault={handleSubmit}>
    <section>
      <label for="command">Command</label>
      <select id="command" bind:value={component}>
        <option value="">Select Command</option>
        {#each commands as command}
          <option value={command.component}>{command.description}</option>
        {/each}
      </select>
    </section>
    <svelte:component this={component} bind:body />
    <button>Send Command</button>
  </form>
</main>

<style>
  main {
    max-width: 480px;
    padding: 24px;
    margin: auto;
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
  }

  img {
    width: 50%;
    margin: 0 auto 32px auto;
  }

  button {
    color: #fff;
    border-color: #2ed573;
    background-color: #2ed573;
  }
</style>
