<script></script>
<div class="item">
    <slot></slot>
</div>
<style lang="scss">
    .item{
        background-color: yellowgreen;
        display: flex;
        height: 6vh;
        width: 3vw;
        margin-left: 25px;
        margin-right: 25px;
        border-radius: 50%;                    
        cursor: pointer;
        &:disabled{
            opacity: 0.4;
            cursor: not-allowed;
        }
        :global(svg){
            fill: #bd1414;
        }
    }
</style>