<script lang="ts">
	import { GradientButton, Img, NavBrand, NavHamburger, NavLi, NavUl, Navbar, P} from "flowbite-svelte";
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
            Hey! We are constantly planning new events and evolving the Society to better itself. Please use the google form below to get in touch.
            Alternatively, feel free to use any of our social channels to give feedback.
            We are always looking to gather feedback on what you think we did well, or what you think we should improve on in the future. 
            This can be in relation to anything, from events to social media posts. Please don't hesitate to get in contact if you have any queries. 
            We will do our best to get back to you as soon as possible, but if we don't manage to catch you on one place please give us a prompt on another outlet.
        </P>
    </div>

    <div class = 'form-container'>
        <iframe 
            src="https://docs.google.com/forms/d/e/1FAIpQLSdLRC-wly-aMvCwlW_MMeR7MqWT-YRkXuT3wYNwPQcFltB7ow/viewform?embedded=true" 
            style="
            min-width: 100%;
            height: 60vh;
            border: none;" 
            title = 'contact-us-form'>
            Loading…</iframe>
    </div>
    <div class = 'centered-container'>
            <Img 
            src={cat_latte.src} 
            alt={cat_latte.alt}
            class="rounded-lg m-5"
            />
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

    .form-container {
        display: flex;
        justify-content: center;
    }
</style>