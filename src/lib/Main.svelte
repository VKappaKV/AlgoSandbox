<script>
    // @ts-ignore
    import MdPerson from 'svelte-icons/md/MdPerson.svelte'
  import SvgIcon from './SvgIcon.svelte';

</script>
<div class="container">
    <div class="alice">
        <SvgIcon icon={MdPerson}/>
    </div>
    <div class="bob">
        <SvgIcon icon={MdPerson}/>
    </div>
</div>

<style lang="scss">
     @use '../styles/variables.scss';
    
    .container{
        display: flex;
        flex: 5;
        /* border: 2px outset variables.$secondary; */
        height: 100%;
    }
    .alice{
        display: flex;
    }
    .alice{
        display: flex;
    }
</style>
