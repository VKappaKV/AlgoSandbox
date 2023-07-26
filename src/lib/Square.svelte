<script>
import ButtonTxn from "./ButtonTxn.svelte";
import Menu from "./Menu.svelte";

</script>

<div>
    <Menu/>
    <ButtonTxn/>
</div>

<style>
    div{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-self: center;
        align-items: center;
/*         width: 1200px;
        height: 800px; */
        width: 50vw;
        height: 80vh;
        border-radius: 20px;
        background-color:cadetblue;
    }
</style>