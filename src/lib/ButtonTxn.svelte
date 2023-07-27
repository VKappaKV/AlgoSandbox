<script>
  import Toast from "./Toast.svelte";

    let buttonText ;
    let timerId = null;
    let isHolding = false;
    let txnConfirmed = false;
    let wasSent = false;
  
    function handleMousedown() {
      isHolding = true;
      timerId = setTimeout(() => {
        triggerHoldEvent();
      }, 1000);
      txnConfirmed = false;
    }
  
    function handleMouseup() {
      isHolding = false;
      clearTimeout(timerId);
    }
  
    function triggerHoldEvent() {
        txnConfirmed = true
        wasSent = true
        handleMouseup()
        setTimeout(()=>{
          txnConfirmed = false;
        }, 3000);
      // Qui puoi triggerare qualsiasi azione o evento desideri
    }
  $: isHolding ? buttonText = 'HOLD' : buttonText = 'SEND';
  $: wasSent ? 
  setTimeout(()=>{
          wasSent = false;
        }, 3000) : null;
  </script>
  
  <style lang="scss">
    @use '../styles/variables.scss';
    button {
      position: relative;
      padding: 10px 20px;
      margin-bottom: 10px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: variables.$secondary;
      color: white;
      cursor: pointer;
      overflow: hidden;
      &:disabled{
        cursor: not-allowed;
        &:hover{
          background-image:linear-gradient(rgba(0,0,0,0.4) 0 0);
        }
      }
    }
  
    button:after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 0;
      height: 100%;
      background-image: linear-gradient(rgba(0,0,0,0.4) 0 0);
      transition: width 0.1s linear; /* Transizione più rapida quando il pulsante non è premuto */
    }
  
    button.holding:after {
      width: 100%;
      transition: width 1s linear; /* Transizione più lenta quando il pulsante è premuto */
    }
  </style>
  
  <button
    class:holding={isHolding}
    disabled={wasSent}
    on:mousedown={handleMousedown}
    on:mouseup={handleMouseup}
    on:mouseleave={handleMouseup}
  >
    {buttonText}
  </button>
  {#if txnConfirmed}
    <Toast>Transaction Sent</Toast>
  {/if}