<script lang="ts">
    import { goto } from '$app/navigation'
    import { GradientButton, Img, TabItem, Tabs } from 'flowbite-svelte'
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
    const college = {
        alt: 'trinity college chapel',
        src: 'https://i.imgur.com/sJWGk0S.jpg'
    }
    import logo from '$lib/assets/logo.jpeg'

    function contactUsHandler(): Promise<void> {
        return goto('/contact-us');
    }
</script>

<body>
<!--Nav Bar -->
    <div class = "nav-bar">
        <Navbar let:hidden let:toggle rounded>
            <NavBrand href="/">
            <img src={logo} class="mr-3 h-6 sm:h-12" alt="CATS Logo" />
            <span class="self-center whitespace-normal text-2xl font-extrabold dark:text-white">Cambridge University Coffee and Tea Society</span>
            </NavBrand>
            <NavHamburger on:click={toggle} />
            <NavUl {hidden}>
            <NavLi href="/" class = 'font-extrabold'>Home</NavLi>
            <NavLi href="#about" class = 'font-extrabold'>About</NavLi>
            <NavLi href="#committee" class = 'font-extrabold'>Committee</NavLi>
            <NavLi href="#connect" class = 'font-extrabold'>Connect</NavLi>
            <NavLi href="/contact-us" class = 'font-extrabold'>Contact Us</NavLi>
            <NavLi href="/mailing-list" class = 'font-extrabold'>Mailing List</NavLi>
            </NavUl>
        </Navbar>
    </div>
    <!-- Header with image -->
    <div class="centered-container">
        <Img 
        src={banner.src} 
        alt={banner.alt} 
        size = 'max-w-2xl'
        class="body-image rounded-lg m-5"
        />
    </div>
    <div class = 'centered-container'>
        <div class = 'text'>
            <Heading 
                customSize="text-6xl font-extrabold"
                class = 'm-5'
                tag = 'h1'
                align = 'center'>
                Cambridge University <Span gradient>Coffee and Tea Society</Span>
            </Heading>
        </div>
    </div>

    <!-- Main Body-->
    <Heading tag="h2" customSize="text-4xl font-extrabold " id = 'about' class = "m-5 underline">About us:</Heading>
    <div class = 'list'>
        <List tag="ul" class="space-y-1 m-5 text-xl">
            <Li>We are a Society within the University of Cambridge hoping to unite students through love of teas and coffees.</Li>
            <Li>Our society gives members a chance to try new varieties and brew methods, as well as a chance to promote improving mental health and wellbeing.</Li>
            <Li>A great way to escape from studies, to take an hour off to speak with friends and make new ones! We are really excited to expand this community with your help.</Li>
            <Li>The society believe that tea and coffee represent more than just a beverage, as the ritual behind pausing your workflow to make these drinks allows you to take a small but important break from your busy day.</Li>
            <Li>Education surrounding ethical and sustainable production of coffee and tea is also massively important and is applicable to many other products too.</Li>
            <Li>One of core our values surrounds choosing to spend the little extra to ensure an improved quality of life for the farmers and workers within the supply chain.</Li>
        </List>
    </div>
    <Heading tag="h2" customSize="text-4xl font-extrabold " id = 'about' class = "m-5 underline">Our industry sponsors:</Heading>
    <div class="centered-container">
        <div class = 'list'>
            <List tag = 'ul' class = 'space-y-1 m-5 font-extrabold text-3xl'>
                <Li><A href="https://www.nichecoffee.co.uk/" color = 'black'>Niche Coffee</A></Li>
                <Li><A href="https://www.aeropress.co.uk/" color = 'black'>AeroPress</A></Li>
                <Li><A href="https://www.uniterra-nomad.com/" color = 'black'>UniTerra</A></Li>
                <Li><A href="https://acaia.co/" color = 'black'>Acaia</A></Li>
                <Li><A href="https://1zpresso.coffee/" color = 'black'>1Zpresso</A></Li>
            </List>
        </div>
        <div class = 'image'><Img 
        src = {sponsors.src}
        alt = {sponsors.alt} 
        size = 'max-w-xl'
        class="body-image m-5"
        />
        </div>
    </div>
    <div class = 'text'>
        <P class = 'm-5 text-xl'>
            We have hopes to work with more companies within industry in the future! 
            We host interesting and unique events such as AeroPress championships, frequent socials, social swaps, cupping events and coffee tournaments.
        </P>
    </div>
    <div class = 'role-box m-10' id = 'committee'>
        <P class = 'mb-5 text-4xl font-extrabold underline'>
            Our committee & role descriptions:
        </P>
          <Tabs style="pill">
            <TabItem open>
              <div slot="title" class="flex items-center gap-2">
                Current Committee
              </div>
              <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                <b>President:</b> <br/>    
                Callum Stephenson - css47 <br/>
                Third year Chemical Engineering student at Trinity
              </p>
              <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                <b>Vice President:</b> <br/>    
                Imane Jaaouine - ij273 <br/>
                Third year Chemical Engineering student at Lucy Cavendish
              </p>
              <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                <b>Senior Treasurer:</b> <br/>    
                Axel Zeitler - jaz22 <br/>
                Chemical Engineering Professor working at Gonville & Caius interested in the applications of TeraHertz
              </p>
              <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                <b>Events Officer:</b> <br/>    
                Role Empty <br/>
              </p>
              <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                <b>Secretary:</b> <br/>    
                Role Empty <br/>
              </p>
            </TabItem>
            <TabItem open>
                <div slot="title" class="flex items-center gap-2">
                  Role Descriptions
                </div>
                <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                    <b>President:</b> <br/>    
                    The President's role within the Society to keep track of everything in a more general aspect than the specified roles, to make decisions with the Society's best interest in mind. 
                    Keep things ticking over properly.
                  </p>
                <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                    <b>Vice President:</b> <br/>    
                    Similar to the president's role, Vice-President is a role about overall societal management - lending a key eye to help the President make the right decision.
                </p>
                <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                    <b>Senior Treasurer:</b> <br/>    
                    The Senior Treasurer's role is to ensure the societies funds are not mismanaged, and to review any appeals from members who have been excluded from the society. 
                    They also allow us to have a bank account and often helps host the AGM.
                </p>
                <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                    <b>Events Officer:</b> <br/>    
                    The Events officer helps plan and run events to ensure that everyone can enjoy themselves and feel included and welcomed!
                </p>
                <p class="text-sm text-gray-500 dark:text-gray-400 m-2">
                    <b>Secretary:</b> <br/>    
                    The Secretary's role is to keep everything organised, plan out event venues, notify members about events, answer emails and managing sponsorships.
                </p>
              </TabItem>
          </Tabs>
    </div>
    <div class = 'centered-container'>
        <Img 
        src={college.src} 
        alt={college.alt} 
        size = 'max-w-xl'
        class="body-image rounded-lg m-5"
        />
    </div>

    <div class="socials-bar" id = "connect">
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
    <div class="horizontally-centered-container m-2">
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