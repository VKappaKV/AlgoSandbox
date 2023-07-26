<script>
import ButtonTxn from "./ButtonTxn.svelte";
  import Explorer from "./Explorer.svelte";
  import Main from "./Main.svelte";
import Menu from "./Menu.svelte";

</script>

<div class="square">
    <Menu/>
    <div class="main-container">
        <Main/>
        <Explorer/>
    </div>
    <div class="footer">
    <ButtonTxn/>
    </div>
</div>

<style lang="scss">
        @use '../styles/variables.scss';

    div{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-self: center;
        align-items: center;
/*         width: 1200px;
        height: 800px; */
        width: 800px;
        height: 800px;
        border-radius: 20px;
        background-color:variables.$tertiary;
    }
    .square{
        border:6px solid variables.$main;
    }
    .main-container{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
    .footer{
        display: flex;
        justify-content: center;
        align-items: center;
        border-end-start-radius: 10px;
        height:10%;
    }
</style>