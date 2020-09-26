<script>
  import { Textfield } from 'svelte-mui';
  import { boardingCard } from './store.js';
</script>

<Textfield
  autocomplete="off"
  label="Host"
  required
  bind:value={$boardingCard.host} />
<Textfield
  autocomplete="off"
  label="Guest"
  required
  bind:value={$boardingCard.guest} />
<Textfield
  autocomplete="off"
  label="Occasion"
  required
  bind:value={$boardingCard.occasion} />

<textarea class="textarea" rows="4" value={$boardingCard.location} />

<Textfield
  autocomplete="off"
  label="Directions"
  required
  bind:value={$boardingCard.directions} />
<Textfield
  autocomplete="off"
  label="Tel"
  required
  bind:value={$boardingCard.phone} />

<label for="meeting-time">
  Date and Starting Time:
  <input type="datetime-local" bind:value={$boardingCard.dateTime} />
</label>

<p>{JSON.stringify($boardingCard, 0, 2)}</p>
