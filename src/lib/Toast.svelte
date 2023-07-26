<script>
    import { onMount, onDestroy } from 'svelte';
    
    let visible = false;
    let timeoutId = null;
    
    onMount(() => {
      visible = true;
      timeoutId = setTimeout(() => {
        visible = false;
      }, 600); // Il toast scompare dopo 2.5 secondi
    });
  
    // Pulisci il timeout quando il componente viene distrutto
    onDestroy(() => {
      if (timeoutId) {
        clearTimeout(timeoutId);
      }
    });
  </script>
  
  <style lang="scss">
     @use '../styles/variables.scss';

    .toast {
      position: fixed;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      background-color: variables.$tertiary;
      color: variables.$background;
      padding: 10px;
      border-radius: 5px;
      opacity: 0;
      transition: opacity 0.8s ease;
      z-index: 1000;
    }
  
    .toast.visible {
      opacity: 1;
    }
  </style>
  
  <div class="toast" class:visible={visible}>
    <slot></slot>   
  </div>
  