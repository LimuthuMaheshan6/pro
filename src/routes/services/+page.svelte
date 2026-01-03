<script lang="ts">
    import "./+page.scss"

    function serviceRouting(n:number) {
        let items = document.querySelectorAll(".route1-service")

        items.forEach(item => item.classList.add("display-none"))

        items[n].classList.remove("display-none")
    }


</script>

<br><br>

<div class="black"></div>
<section class="box components">
    <h1 class="heading1-service" style="text-align: center; color:white; padding-bottom: 20px;">What You'll Get</h1>
 



    <div class="grid-service">

        <div class="grid2-service">
            <div class="res-s">
                <h2 class="heading2-service">Fast Websites</h2>
                <p class="service-p">Performance Focused. Doesn't have to worry about speed.</p>
            </div>
            <div >
                <img class="img" src="images/high.webp"  alt="high performance">
            </div>
        </div>


    </div>

    <hr>


     <div class="grid-service">

        <div class="grid2-service-reverse">
            <div class="res-s" style="margin-top: 30px;">
                <h2 class="heading2-service">Responsive Navbars</h2>

                <p class="service-p">Overcome the complexity of building a navbar</p>
            </div>
            <div>
                <div class="service-navbar1" style="margin-top: 90px;">
                    <div class="nav-s">
                        <button id="btn-s" class="ham-s" aria-label="b" on:click={
                            () => {
                                let btn = document.getElementById("btn-s")
                                let pad = document.getElementById("pad-s")

                                pad?.classList.toggle("display-none")

                                btn?.classList.toggle("open-s")
                            }
                        }>
                            <div class="ham-st"></div>
                            <div class="ham-sm"></div>
                            <div class="ham-sb"></div>

                        </button>
                        <div style="transform: translateY(-9px);">
                            <p>Logo</p>
                        </div>
                        <div style="transform: translateY(-9px); margin-right: 9px;">
                            <p>CTA</p>
                        </div>
                    </div>
                </div>
                <div id="pad-s" class="display-none pad-s">
                
                </div>
            </div>
            

        </div>


    </div>

    <hr>

            <div class="grid-service">

        <div class="grid2-service">
            <div class="res-s" style="margin-top: 30px;">
                <h2 class="heading2-service">Powerful Navigation</h2>

                <p class="service-p">Imagine the burden of getting a one page scroll web without page navigation.</p>
            </div>
          
               <div class="route-service">
                  <div class="s106">
                    <div style="margin-left: 10px;"></div>
                     <div class="s108">
                         <button on:click={() => serviceRouting(0)}>Home</button>
                         <button on:click={() => serviceRouting(1)}>Pricing</button>
                         <button on:click={() => serviceRouting(2)} >About</button>
                         <button on:click={() => serviceRouting(3)}>Contact</button>
                     </div>
                     <div style="margin-right: 10px;"></div>
                  </div>

                  <div class="route1-service"><div class="r110"><b>Home</b></div><br>Hello! Welcome. You are in home</div>
                  <div class="display-none route1-service"><div class="r110"><b>Pricing</b></div> <br>Affordable pricing. Starting from $10.</div>
                  <div class="display-none route1-service"><div class="r110"><b>About</b></div> <br>A business that works for your financial freedom.</div>
                  <div class="display-none route1-service"><div class="r110"><b>Contact Information</b></div> <br>Name: Limuthu Maheshan <br> Number: +94 703143435</div>


               </div>
       
            

        </div>


    </div>

    <hr>
        <div class="grid-service">

        <div class="grid2-service-reverse">
            <div class="res-s" style="margin-top: 30px;">
                <h2 class="heading2-service">Hosting With Domain</h2>

                <p class="service-p">Helping you in hosting and domain name registry.</p>
            </div>
            <div>
               <h2 style="margin-bottom: 0px;">.com  .lk  .net</h2>
               <h2>.org   .info</h2>
                    
            </div>
            

        </div>


    </div>

    <hr>

     <div class="grid-service">

        <div class="grid2-service">
            <div class="res-s">
                <h2 class="heading2-service">Premium Designs</h2>
                <p class="service-p">User friendly design based on your purpose, branding and colour themes.</p>
            </div>
            <div >
                <img class="img" src="images/Design.webp" width="400px" alt="high performance">
            </div>
        </div>


    </div>

    <hr>

 
</section>