<script lang="ts">
    import "./+page.scss"

    function headButtonHandler(n: number) {
                let p17 = document.querySelectorAll(".p17")
                let tail = document.querySelectorAll(".tail")

                if (!tail[n].classList.contains("display-none")) {
                    tail[n].classList.add("display-none")
                    p17[n].classList.remove("open-15")
                    return "hello"
                }
                
                

             
                tail.forEach((item, index) => {
                    item.classList.add("display-none")
                    p17[index].classList.remove("open-15")
                })
             

                tail[n]!.classList.toggle("display-none")
                    
                p17[n]!.classList.toggle("open-15") 



             
                

              
    }


</script>

<br><br>
<h1 style="text-align: center;">Frequently Asked Questions</h1>

<section class="port21">

   
        <div class="port43" >
            <button class="head" aria-label="d" on:click={() => headButtonHandler(0)}>
               
                <div>
                    <p style="color: white; text-transform:capitalize;">Why performance ?</p>
                </div>
                <div id="p17" class="p17">
                   <div class="plus-1"></div>
                   <div class="plus-2"></div>

                </div>

            </button>
            <div class="display-none tail">
                <p style="color: black; margin: 0px; padding: 20px; text-align:justify">
                    Performance is everything these days. Faster page loads are crucial for SEO and customer satisfaction. 
                    There's nothing that gets benefited by performance than marketing.
                </p>
            </div>
        </div>

        <div class="port43" >
            <button class="head" aria-label="d" on:click={() => headButtonHandler(1)}>
             
                <div>
                    <p style="color: white; text-transform:capitalize;">How much the price ?</p>
                </div>
                <div id="p17" class="p17">
                   <div class="plus-1"></div>
                   <div class="plus-2"></div>

                </div>

            </button>
            <div class="display-none tail">
                <p style="color: black; margin: 0px; padding: 20px; text-align:justify">
                    Well. It depends.
                </p>
            </div>
        </div>


        
        <div class="port43" >
            <button class="head" aria-label="d" on:click={() => headButtonHandler(2)}>
             
                <div>
                    <p style="color: white; text-transform:capitalize;">About My experience ?</p>
                </div>
                <div id="p17" class="p17">
                   <div class="plus-1"></div>
                   <div class="plus-2"></div>

                </div>

            </button>
            <div class="display-none tail">
                <p style="color: black; margin: 0px; padding: 20px; text-align:justify">
                    10 years of coding experience. Now, has navigated into different langauges like javascript,
                    python, typescript, golang and many.
                </p>
            </div>
        </div>

                
        <div class="port43" >
            <button class="head" aria-label="d" on:click={() => headButtonHandler(3)}>
           
                <div>
                    <p style="color: white; text-transform:capitalize;">Will it improve my business / job ?</p>
                </div>
                <div id="p17" class="p17">
                   <div class="plus-1"></div>
                   <div class="plus-2"></div>

                </div>

            </button>
            <div class="display-none tail">
                <p style="color: black; margin: 0px; padding: 20px; text-align:justify">
                    First of all. Tell me how many people have their personal websites. Only few. Ofcourse! 
                    it improves your business revenues / job interview success. 
                </p>
            </div>
        </div>


                        
        <div class="port43" >
            <button class="head" aria-label="d" on:click={() => headButtonHandler(4)}>
           
                <div>
                    <p style="color: white; text-transform:capitalize;">Personal Benefit ?</p>
                </div>
                <div id="p17" class="p17">
                   <div class="plus-1"></div>
                   <div class="plus-2"></div>

                </div>

            </button>
            <div class="display-none tail">
                <p style="color: black; margin: 0px; padding: 20px; text-align:justify">
                    A website helps you to position yourself as number 1. This will increase revenues. 
                    That helps your family a lot. May help you to enjoy life as time is saved. 

                </p>
            </div>
        </div>
      
    
 

    
</section>


