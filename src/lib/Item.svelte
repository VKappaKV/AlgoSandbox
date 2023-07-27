<script></script>
<div class="item">
    <div class="content">
        <slot></slot>
    </div>
</div>
<style lang="scss">
    @use '../styles/variables.scss';
    .item {
        background-color: variables.$secondary;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 3vw;  /* Controllo la larghezza */
        height: 0;   /* Imposto l'altezza a 0 */
        padding-bottom: 3vw; /* Imposto il padding-bottom alla stessa dimensione della larghezza */
        margin-left: 25px;
        margin-right: 25px;
        border-radius: 50%;
        border: 2px outset variables.$details;
        cursor: pointer;
        position: relative; /* Aggiungo la posizione relativa per permettere al contenuto di posizionarsi all'interno */
        &:disabled{
            opacity: 0.4;
            cursor: not-allowed;
        }

        .content {
            position: absolute; /* Posiziono assolutamente il contenuto all'interno dell'elemento */
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            display: flex;  /* Utilizzo flex per centrare il contenuto */
            justify-content: center;
            align-items: center;
        }
    }
</style>