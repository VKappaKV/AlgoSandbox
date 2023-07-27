<!-- SvgIcon.svelte -->
<script>
    export let icon = null;
  </script>
  
  <div class="svg-icon">
    <svelte:component this={icon} />
  </div>
  
  <style lang="scss">
    @use '../styles/variables.scss';
    .svg-icon {
      color: variables.$details;
      width: 50%;
      height: 50%;
      padding: 2px;
    }
  </style>
  