<script>
  import Item from "./Item.svelte";
  // @ts-ignore
  import FaRegHandPointRight from 'svelte-icons/fa/FaRegHandPointRight.svelte'
  // @ts-ignore
  import FaRegHandPointLeft from 'svelte-icons/fa/FaRegHandPointLeft.svelte'
  import SvgIcon from "./SvgIcon.svelte";
  import { BottomNav, BottomNavItem, Tooltip } from "flowbite-svelte"
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
<!-- <BottomNav  navType="application" classInner="grid-cols-5">
    <BottomNavItem btnName="Home" appBtnPosition="left">
        <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"></path>
        </svg>
        <Tooltip arrow={false}>Home</Tooltip>
    </BottomNavItem>
    <BottomNavItem btnName="Wallet" appBtnPosition="middle">
        <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path d="M4 4a2 2 0 00-2 2v1h16V6a2 2 0 00-2-2H4z"></path>
          <path clip-rule="evenodd" fill-rule="evenodd" d="M18 9H2v5a2 2 0 002 2h12a2 2 0 002-2V9zM4 13a1 1 0 011-1h1a1 1 0 110 2H5a1 1 0 01-1-1zm5-1a1 1 0 100 2h1a1 1 0 100-2H9z"></path>
        </svg>
        <Tooltip arrow={false}>Wallet</Tooltip>
    </BottomNavItem>
    <div class="flex items-center justify-center">
      <BottomNavItem btnName="Create new item" appBtnPosition="middle" btnClass="inline-flex items-center justify-center w-10 h-10 font-medium bg-primary-600 rounded-full hover:bg-primary-700 group focus:ring-4 focus:ring-primary-300 focus:outline-none dark:focus:ring-primary-800">
          <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path clip-rule="evenodd" fill-rule="evenodd" d="M10 3a1 1 0 011 1v5h5a1 1 0 110 2h-5v5a1 1 0 11-2 0v-5H4a1 1 0 110-2h5V4a1 1 0 011-1z"></path>
          </svg>
        <Tooltip arrow={false}>Create new item</Tooltip>
      </BottomNavItem>
    </div>
    <BottomNavItem btnName="Settings" appBtnPosition="middle">
        <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path d="M5 4a1 1 0 00-2 0v7.268a2 2 0 000 3.464V16a1 1 0 102 0v-1.268a2 2 0 000-3.464V4zM11 4a1 1 0 10-2 0v1.268a2 2 0 000 3.464V16a1 1 0 102 0V8.732a2 2 0 000-3.464V4zM16 3a1 1 0 011 1v7.268a2 2 0 010 3.464V16a1 1 0 11-2 0v-1.268a2 2 0 010-3.464V4a1 1 0 011-1z"></path>
        </svg>
      <Tooltip arrow={false}>Settings</Tooltip>
    </BottomNavItem>
    <BottomNavItem btnName="Profile" appBtnPosition="right">
        <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path clip-rule="evenodd" fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.084A5 5 0 0010 11z"></path>
        </svg>
        <Tooltip arrow={false}>Profile</Tooltip>
    </BottomNavItem>
  </BottomNav>
 -->
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