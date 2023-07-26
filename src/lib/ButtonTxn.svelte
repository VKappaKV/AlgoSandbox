<script>
  import Toast from "./Toast.svelte";

    let buttonText = 'Click Me';
    let timerId = null;
    let isHolding = false;
    let txnConfirmed = false;
  
    function handleMousedown() {
      isHolding = true;
      buttonText = 'HOLD';
      timerId = setTimeout(() => {
        triggerHoldEvent();
      }, 1000);
      txnConfirmed = false;
    }
  
    function handleMouseup() {
      isHolding = false;
      clearTimeout(timerId);
      buttonText = 'Click Me';
    }
  
    function triggerHoldEvent() {
        txnConfirmed = true
        handleMouseup()
      // Qui puoi triggerare qualsiasi azione o evento desideri
    }
  </script>
  
  <style>
    button {
      position: relative;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: #4CAF50;
      color: white;
      cursor: pointer;
      overflow: hidden;
    }
  
    button:after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 0;
      height: 100%;
      background-color: #2E7D32;
      transition: width 0.1s linear; /* Transizione più rapida quando il pulsante non è premuto */
    }
  
    button.holding:after {
      width: 100%;
      transition: width 1s linear; /* Transizione più lenta quando il pulsante è premuto */
    }
  </style>
  
  <button
    class:holding={isHolding}
    on:mousedown={handleMousedown}
    on:mouseup={handleMouseup}
    on:mouseleave={handleMouseup}
  >
    {buttonText}
  </button>
  {#if txnConfirmed}
  <Toast>Hai completato l'operazione</Toast>
  {/if}