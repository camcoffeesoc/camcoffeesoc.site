<script lang="ts">
    import { goto } from '$app/navigation'
    import { GradientButton, Img } from 'flowbite-svelte'
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
    import { Heading, Span, P, List, Li, A} from 'flowbite-svelte';

    const banner = {
        alt: 'coffee-brewer',
        src: 'https://i.imgur.com/dD2SBle.png'
    };
    const sponsors = {
        alt: 'our sponsors as listed above',
        src: 'https://i.imgur.com/7Z7RQnP.png'
    }
    const cat_latte = {
        alt: 'cat latte art',
        src: 'https://i.imgur.com/kLgUtDa.png'
    }
    import logo from '$lib/assets/logo.jpeg'

    function contactUsHandler(): Promise<void> {
        return goto('/contact-us');
    }
</script>

<body>
<!--Nav Bar -->
<Navbar let:hidden let:toggle>
    <NavBrand href="/">
      <img src={logo} class="mr-3 h-6 sm:h-12" alt="CATS Logo" />
      <span class="self-center whitespace-nowrap text-xl font-extrabold dark:text-white">Cambridge University Coffee and Tea Society</span>
    </NavBrand>
    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="#">Home</NavLi>
      <NavLi href="#about">About</NavLi>
      <NavLi href="#commitee">Commitee</NavLi>
      <NavLi href="#connect">Connect</NavLi>
    </NavUl>
</Navbar>

<!-- Header with image -->
<div class="header-container">
    <Img 
        src={banner.src} 
        alt={banner.alt} 
        size = 'max-w-xs'
        class="rounded-lg m-3"
        />
    <Heading 
        customSize="text-3xl font-extrabold  md:text-5xl lg:text-5xl"
        class = 'm-2'
        tag = 'h1'
        align = 'center'>
        Cambridge University <Span gradient>Coffee and Tea Society</Span>
    </Heading>
</div>

<!-- Main Body-->
<Heading tag="h2" customSize="text-4xl font-extrabold " id = 'about' class = "m-3">About us</Heading>
<List tag="ul" class="space-y-1 m-3 text-xl">
    <Li>We are a Society within the University of Cambridge hoping to unite students through love of teas and coffees.</Li>
    <Li>Our society gives members a chance to try new varieties and brew methods, as well as a chance to promote improving mental health and wellbeing.</Li>
    <Li>A great way to escape from studies, to take an hour off to speak with friends and make new ones! We are really excited to expand this community with your help.</Li>
    <Li>The society believe that tea and coffee represent more than just a beverage, as the ritual behind pausing your workflow to make these drinks allows you to take a small but important break from your busy day.</Li>
    <Li>Education surrounding ethical and sustainable production of coffee and tea is also massively important and is applicable to many other products too.</Li>
    <Li>One of our values surrounds choosing to spend the little extra to ensure an improved quality of life for the farmers and workers within the supply chain.</Li>
</List>
<Heading tag="h2" customSize="text-4xl font-extrabold " id = 'about' class = "m-3">Our industry sponsors:</Heading>
<div class = 'sponsor-container'> 
    <List tag = 'ul' class = 'space-y-1 m-3 font-extrabold text-3xl'>
        <Li><A href="https://www.nichecoffee.co.uk/" color = 'black'>Niche Coffee</A></Li>
        <Li><A href="https://www.aeropress.co.uk/" color = 'black'>AeroPress</A></Li>
        <Li><A href="https://www.uniterra-nomad.com/" color = 'black'>UniTerra</A></Li>
        <Li><A href="https://acaia.co/" color = 'black'>Acaia</A></Li>
        <Li><A href="https://1zpresso.coffee/" color = 'black'>1Zpresso</A></Li>
    </List>
    <Img 
        src = {sponsors.src}
        alt = {sponsors.alt} 
        size = 'max-w-xl'
        class="rounded-lg m-3"/>
</div>
<P class = 'm-3 text-xl'>
    We have hopes to work with more companies within industry in the future! 
    We host interesting and unique events such as AeroPress championships, frequent socials, social swaps, cupping events and coffee tournaments.
</P>
<div class="socials-bar" id = "connect">
    <GradientButton 
        outline
        color="purpleToBlue"
        href="https://www.instagram.com/camcoffeesoc/"
        class ="m-1">
            <i
                class ="fa-brands fa-instagram fa-2x"  
                aria-label="instagram"
                />
    </GradientButton>

    <GradientButton 
        outline 
        color="purpleToBlue"
        href="https://discord.gg/XddmUQcBTg"
        class ="m-1">
        <i 
            class ="fa-brands fa-discord fa-2x" 
            aria-label="discord"
            />
    </GradientButton>

    <GradientButton 
        outline 
        color="purpleToBlue"
        href="https://chat.whatsapp.com/FJdT89pET9mBL0WHKlNhaz"
        class ="m-1">
        <i 
            class ="fa-brands fa-whatsapp fa-2x" 
            aria-label="whatsapp"
            />
    </GradientButton>

    <GradientButton 
        outline 
        color="purpleToBlue"
        href="mailto:camcoffeesoc@gmail.com"
        class = "m-1">
        <i 
            class= "fa fa-envelope-o fa-2x" 
            aria-label="mail"
            />
    </GradientButton>
</div>
<div class="generic-container">
    <GradientButton 
        color="purpleToBlue"
        class = 'text-4xl'
        on:click={() => contactUsHandler()}
        >
        Contact Us
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
    @import 'styles.scss';
</style>