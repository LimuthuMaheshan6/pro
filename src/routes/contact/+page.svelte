<script lang="ts">
    import { onMount } from "svelte";


    import {z} from "zod";

 
    const User = {
       email: z.string().email(),
       number: z.string().min(2)
    };
    
    
    
    let form = {
        
        email: "", 
        number: ""
    }

    
    $:errUser = {
        email: !User.email.safeParse(form.email).success,
        number: !User.number.safeParse(form.number).success,

    }
    // the parsed result is validated and type safe!
  
    
    // so you can use it with confidence :)
    


</script>


<br><br>
<h1 style="text-align: center;  line-height: 1;">Contact Us</h1>


<section style="display: flex; flex-direction: column; align-items: center; ">


<div class="">
    
    <p style="text-align: center; font-weight: 300">Tell us about you</p>
        <form on:submit={(e) => {
            e.preventDefault()


            console.log("submited...")
            
                
        }}>
            <input bind:value={form.email} type="email" placeholder="Email"> 
            {#if form.email && !User.email.safeParse(form.email).success}
                <p style="margin: 0; font-size: 11px; color: red;">Need correct form of email</p>
            {/if}
            <br><br>
            <input bind:value={form.number} type="tel" placeholder="Whatsapp Number">
            {#if form.number && !User.number.safeParse(form.number).success}
                <p style="margin: 0; font-size: 11px; color: red;">Type your phone number</p>
                
            {/if}
            <br><br>
    
        <button class= {(!(User.email.safeParse(form.email).success) || !User.number.safeParse(form.number).success) ? "con-btn ":"con-btn-active "}  disabled={errUser.email || errUser.number} type="submit">Send</button>
        </form>
    
</div>
</section>


<br>

<section style="background: #000; color: white; padding-top: 30px; padding-bottom: 600px;">
    <a style="text-decoration: none; color: white;" href="tel:940703143435">
        <p style="text-align: center; line-height: 1;">Call: +94 703143435</p>
    </a>
    <p style="text-align: center; line-height: 1;">Name:Limuthu Maheshan</p>
</section>



<style> 
    input {
        outline: none;
        border-radius: 6px;
        padding: 6px;
        border: 2px solid black;
        width: 250px;
        font-size: 18px;
    }

    .con-btn {
       
        padding: 10px;
        cursor: pointer;
        color: white;
        border: none;
        font-size: 16px;
        border-radius: 12px;
        background: rgba(0, 128, 0, 0.384);
        



    }

     .con-btn-active {
       
        padding: 10px;
        cursor: pointer;
        color: white;
        border: none;
        font-size: 16px;
        border-radius: 12px;
        background: rgb(0, 128, 0);
        



    }


  
</style>