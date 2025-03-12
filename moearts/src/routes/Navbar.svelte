<script>
  import Logo from "$lib/images/svg/Logo_NB.svg";
  import { Menu, X } from "@lucide/svelte";
  let isOpen = false;

  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<nav class="menu-box">
  <div class="menu">
    <a class="logo" href="/"
      ><div class="logo">
        <img class="moe" src={Logo} alt="logo" width="24px" />GaiaMoe
      </div></a
    >
    <div class="links">
      <a href="/">Works</a>
      <a href="/">About</a>
      <a href="/">Contact</a>
    </div>
  </div>
  <button class="menu-button, compressed-menu" on:click={toggleMenu}>
    <a href="#"><Menu class="menu-icon" /></a>
  </button>
</nav>

{#if isOpen}
  <div class="compressed-menu">
    <a href="#" on:click={toggleMenu}></a>
  </div>
{/if}
<div class="sidebar {isOpen ? 'open' : ''}">
  <div class="sidebar-top">
 <!--  <button class="close-button" on:click={toggleMenu}>
    <a href="#" class="close-icon"><X size={32}/></a>
  </button> --></div>
  <div class="sidebar-voices">
    <a class="sidebar-voice" href="/">WORKS</a>
    <a class="sidebar-voice" href="/">ABOUT</a>
    <a class="sidebar-voice" href="/">CONTACT</a>
  </div>
</div>

<style>
 
  button {
    box-shadow: none;
    border: none;
    background: none;
  }

  a {
    text-decoration: none;
    color: #F7F7F7;
    margin: 0 16px;
    transition: 0.3s;
  }
  a:hover {
    text-decoration: none;
    color: #5863F8;
    transition: 0.3s;
  }
  .menu-box {
    width: 100%;
    position: fixed;
    top: 0px;
    display: flex;
    z-index: 10;
  }
  .menu {
    width: 100%;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    font-size: 16px;
    font-weight: 300;
    background-color: #1B1B1B;
    color: #F7F7F7;
  }
  
  .compressed-menu {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    background-color: #1B1B1B;
    color: #F7F7F7;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 16px;
    font-size: 24px;
    font-weight: 400;
  }
  div .logo {
    font-size: 24px;
    font-weight: 400;
  }

  .links a {
    margin: 0 48px;
    transition: 0.3s;
  }
  .links a:hover {
    color: #F7F7F79c;
    transition: 0.3s;
  }

  .links a:last-child {
    margin: 0 16px;
  }

  .sidebar {
    position: fixed;
    top: 0;
    right: -150%; /* Nasconde il menu fuori dallo schermo */
    width: 100%;
    height: 100vh;
    background: #1B1B1B;
    transition: right 0.3s ease-in-out;
    padding: 30px 0;
    padding-left: 32px;
    z-index: 6;
  }

  .sidebar.open {
    right: 0; /* Quando è aperto, lo sposta in vista */
  }

  .sidebar-top
  {
    display: flex;
    justify-content: end;
    flex-direction: row-reverse;
    align-items: center;
    padding-bottom: 32px;
  }
  .sidebar-voices
  {
    display: flex;
    flex-direction: column;
    gap: 48px;
    justify-content: center;
    align-items: center;
  }
  .sidebar-voice{
    font-size: 72pt;
    font-weight: 700;
    transition: 0.3s;
  }
  .sidebar-voice:hover{
    color: #5863F8;
    transition: 0.3s;
    
  }
  @media (max-width: 1920px) {
    .compressed-menu {
      display: none;
    }
  }

  @media (max-width: 1100px) {
    .links {
      display: none;
    }

    .compressed-menu {
      display: flex;
    }
    .menu{
      padding: 16px;
    }
  
  div .logo {
    font-size: 16px;
  }
  }
  @media (max-width: 650px) {
    .menu{
      padding: 12px;
    }   
  }
    @media (max-width: 375px) {
       
  }
</style>
