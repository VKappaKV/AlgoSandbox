<script>
  import Item from "./Item.svelte";
  // @ts-ignore
  import FaRegHandPointRight from 'svelte-icons/fa/FaRegHandPointRight.svelte'
</script>
<div class="container">
    <Item><FaRegHandPointRight/></Item>
    <Item></Item>
    <Item></Item>
    <Item></Item>
</div>
<style>
    .container{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 50px;
        flex-wrap: wrap;
        background-color: brown;
        height: 100px;
        width: 100%;
        border-start-start-radius: 20px;
        border-start-end-radius: 20px;
    }
</style>