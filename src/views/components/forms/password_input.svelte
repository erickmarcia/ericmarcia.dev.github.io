<script>
  export let inputName = 'password'
  export let id = 'password'
  export let label = 'Contraseña'
  export let value = ''
  export let icon = 'lock'
  export let error = false
  export let isFocused = false
  export let errorMessage = 'Por favor, añade una contraseña'
  export let helpText = ''
</script>

<div class="input-field">
  {#if icon}
    <i class="material-icons prefix">{icon}</i>
  {/if}
  <input
    bind:value
    on:input={() => (error = false)}
    type="password"
    name={inputName}
    {id}
    class:invalid={error}
    autofocus={isFocused}
    on:blur />
  <label for={id}>{label}</label>
  <span class="helper-text" data-error={errorMessage}>{helpText}</span>
</div>
