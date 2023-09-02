<script lang="ts">
	import { Button, GradientButton, Img, NavBrand, NavHamburger, NavLi, NavUl, Navbar, P} from "flowbite-svelte";
    import logo from '$lib/assets/logo.jpeg';
    const cat_latte = {
        alt: 'cat latte art',
        src: 'https://i.imgur.com/kLgUtDa.png'
    }
</script>
<body>
    <!--Nav Bar -->
    <div class = 'centered-container'>
        <Navbar let:hidden let:toggle rounded>
            <NavBrand href="/">
            <img src={logo} class="mr-3 h-6 sm:h-12" alt="CATS Logo" />
            <span class="self-center whitespace-nowrap text-2xl font-extrabold dark:text-white">Cambridge University Coffee and Tea Society</span>
            </NavBrand>
            <NavHamburger on:click={toggle} />
            <NavUl {hidden}>
            <NavLi href="/" class = 'font-extrabold'>Home</NavLi>
            <NavLi href="../#about" class = 'font-extrabold'>About</NavLi>
            <NavLi href="../#committee" class = 'font-extrabold'>Committee</NavLi>
            <NavLi href="../#connect" class = 'font-extrabold'>Connect</NavLi>
            <NavLi href="/contact-us" class = 'font-extrabold'>Contact Us</NavLi>
            <NavLi href="/mailing-list" class = 'font-extrabold'>Mailing List</NavLi>
            </NavUl>
        </Navbar>
    </div>

    <div class = 'centered-container ml-20 mr-20 mt-3'>
        <P class = 'm-2 font-bold text-xl'>
            We use the student run computing facility to manage our mailing list - please use the link <GradientButton color="purpleToBlue" href="https://lists.srcf.net/mailman/listinfo/camcoffee-news">here</GradientButton> to sign up to our mailing list. <br/>
            If you have any issues with signing up, please get in contact with us at <a href='mailto:camcoffeesoc@gmail.com'>camcoffeesoc@gmail.com</a>, or through any of our socials.
        </P>
    </div>
    <div class="socials-bar m-2" id = "connect">
        <GradientButton 
            outline
            color="purpleToBlue"
            href="https://www.instagram.com/camcoffeesoc/"
            class ="m-1">
                <i
                    class ="fa-brands fa-instagram fa-2x"  
                    aria-Label="instagram"
                    />
        </GradientButton>

        <GradientButton 
            outline 
            color="purpleToBlue"
            href="https://discord.gg/XddmUQcBTg"
            class ="m-1">
            <i 
                class ="fa-brands fa-discord fa-2x" 
                aria-Label="discord"
                />
        </GradientButton>

        <GradientButton 
            outline 
            color="purpleToBlue"
            href="https://chat.whatsapp.com/FJdT89pET9mBL0WHKlNhaz"
            class ="m-1">
            <i 
                class ="fa-brands fa-whatsapp fa-2x" 
                aria-Label="whatsapp"
                />
        </GradientButton>

        <GradientButton 
            outline 
            color="purpleToBlue"
            href="mailto:camcoffeesoc@gmail.com"
            class = "m-1">
            <i 
                class= "fa fa-envelope-o fa-2x" 
                aria-Label="mail"
                />
        </GradientButton>
   </div>
    <div class="footer-container">
        <footer class="page-footer">
            <p>Any incorrect information above? Please let us know via email.</p>
            <p> We hope to see you at our events throughout the year!</p>
        </footer>
    </div>
</body>
<style lang="scss">
    @import '../styles.scss';
</style>