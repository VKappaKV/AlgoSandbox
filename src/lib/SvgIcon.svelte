<!-- SvgIcon.svelte -->
<script>
    export let icon = null;
  </script>
  
  <div class="svg-icon">
    <svelte:component this={icon} />
  </div>
  
  <style>
    .svg-icon {
      width: 50%;
      height: 50%;
    }

  </style>
  