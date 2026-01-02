<script lang="ts">
    import "./Navbar.scss"
    import { page } from "$app/stores";
    import { onMount } from "svelte";

    let path = ""
  

    let links = [
        {path: "/services", name: "Services"},
        {path: "/pricing", name: "Pricing"},
        {path: "/portfolio", name: "Portfolio"},
        {path: "/about", name: "About"},
        

    ]


</script>

<div class="nav">
    
    <div id="navbar" class="navbar">
        <div class="laptop">
            <div class="logo">
                <a href="/">Pro Websites .LK</a>
            </div>
            <div class="links">
                {#each links as item}
                <a class="inactive" class:active={$page.url.pathname === item.path}  href={item.path}>{item.name}</a>
    
                {/each}
    
    
            </div>
            <div class="contact">
                <a href="/contact">Contact</a>
            </div>
    
        </div>
        <div class="mobile">
            <div>
                <button id="ham" class="hamburger " aria-label="nav button"  on:click={() => {
                    let btn = document.getElementById("ham")
                    let pad =  document.getElementById("pad")
                    let navbar = document.getElementById("navbar")
    
    
                    btn?.classList.toggle("open")
                    pad?.classList.toggle("display-none")
                    navbar?.classList.toggle("open-nav")
                }}>
                    <div class="ham1"></div>
                    <div class="ham2"></div>
                    <div class="ham3"></div>
            </button>
            </div>
            <div class="logo">
                <a  href="/" on:click={() => {
                    let pad = document.getElementById("pad")
                    let ham = document.getElementById("ham")



                    pad?.classList.add("display-none")
                    ham?.classList.remove("open")
                }}>Pro Websites .LK</a>
            </div>
            <div class="contact" style="margin-left: -30px;">
                <a  href="/contact" on:click={() => {
                    let pad = document.getElementById("pad")
                    let ham = document.getElementById("ham")

                    pad?.classList.add("display-none")
                    ham?.classList.remove("open")

                }}>Contact</a>
            </div>
    
    
        </div>
    </div>
    
    
    
    
    
    
     <div class="display-none" id="pad">
    
        <div style="height: 70px; width:100%; background:black;"></div>
    
    
         <div class="flex-center">
             {#each links as item}
                    <a class="inactive1" class:active={$page.url.pathname === item.path}  href={item.path}
                    on:click={() => {
                        let ham = document.getElementById("ham")
                        let pad = document.getElementById("pad")
                        pad?.classList.toggle("display-none")
                        ham?.classList.toggle("open")
                    }}>{item.name}</a>
                    <br>
                {/each}
         </div>
    
    </div>
    
</div>

