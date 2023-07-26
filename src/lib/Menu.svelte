<script>
  import Item from "./Item.svelte";
  // @ts-ignore
  import FaRegHandPointRight from 'svelte-icons/fa/FaRegHandPointRight.svelte'
  // @ts-ignore
  import FaRegHandPointLeft from 'svelte-icons/fa/FaRegHandPointLeft.svelte'
  import SvgIcon from "./SvgIcon.svelte";
</script>
<div class="container">
    <Item>
        <SvgIcon icon={FaRegHandPointRight} />
    </Item>
    <Item>
        <SvgIcon icon={FaRegHandPointLeft} />
    </Item>
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
        background-image: linear-gradient(rgba(0,0,0,0.4) 0 0);
        height: 100px;
        width: 100%;
        border-start-start-radius: 20px;
        border-start-end-radius: 20px;
    }
</style>