<script lang="ts">
   

    import Navbar from "$lib/components/Navbar.svelte";
   
    import "./+layout.scss"
    
    import { onMount } from "svelte";
    import { page } from "$app/stores";

    
    import AOS from "aos";
    import "aos/dist/aos.css"
    
    
    onMount( async () => {
       await AOS.init({
           anchorPlacement: "top-center",
            delay: 0,
            
            
            
        })
    })


/*    onMount(async () => {
        let inter = new FontFace("inter", "url(inter.woff2)")

        await inter.load()
        document.fonts.add(inter) 

        


    })  */

    onMount(() => {
        let cursor = document.getElementById("cursor")
        
        document.addEventListener("mousemove", (e) => {
            cursor!.style.left = e.clientX + "px"
            cursor!.style.top  = e.clientY + "px"
        })
    })

    
</script>



<Navbar></Navbar>
<div id="cursor" class="cursor"></div>
<slot></slot>

<section class="junk">
    
    <div class="web">
        <p style="font-size: 47px;">Pro Websites</p>
        <p style="font-size: 18px; color:gray; margin-top: -30px; text-align:center;">We sell the most specialized marketing websites</p>
        
    </div>
    <div style="text-align: center;">
        <p style="font-weight: 600; transform: translateY(18px); ">Help</p> 
        <a class="junk-links" class:active={($page.url.pathname === "/services")} target="_self" href="services">Services</a> <br>
        <a class="junk-links" class:active={($page.url.pathname === "/pricing")} target="_self" href="pricing">Pricing</a> <br>
        <a class="junk-links" class:active={($page.url.pathname === "/portfolio")}  target="_self" href="portfolio">Portfolio</a> <br>
        <a class="junk-links" class:active={($page.url.pathname === "/about")} target="_self" href="about">About</a> <br>
        <a class="junk-links" class:active={($page.url.pathname === "/contact")} target="_self" href="contact">Contact</a> <br>
        
    </div>
</section>