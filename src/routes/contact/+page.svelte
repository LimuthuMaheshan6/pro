<script lang="ts">
    let form = {
        name: "",
        email: "", 
        number: ""
    }
</script>


<br><br>
<h1 style="text-align: center;  line-height: 1;">Contact Us</h1>


<section style="display: flex; flex-direction: column; align-items: center; ">


<div class="">
    
    <p style="text-align: center; font-weight: 300">Tell us about you</p>
        <form action="">
            <input bind:value={form.email} type="text" placeholder="Email"> <br><br>
            <input bind:value={form.number} type="tel" placeholder="Whatsapp Number"><br><br>
    
        <button class="con-btn" type="submit"  on:click={() => {
            console.log("Form: ",form)
        }}>Form Works</button>
        </form>
    
</div>
</section>


<br>

<section style="background: #000; color: white; padding-top: 30px; padding-bottom: 600px;">
    <p style="text-align: center; line-height: 1;">Name:Limuthu Maheshan</p>
    <p style="text-align: center; line-height: 1;">Call: +94 703143435</p>
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
        background: rgb(42, 204, 42);
        color: white;
        border: none;
        font-size: 16px;
        border-radius: 12px;

        



    }


    .con-btn:hover {
        background: green;
    }
</style>