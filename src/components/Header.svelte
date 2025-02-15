<script>
    export let y;

    export let tabs = [
        
        { name: "About ", link: '/about' },
        { name: "Blog", link: "#Blog" },
        { name: "Customers ", link: '/customers' },
        { name: "Resources ", link: "#Resources " },
        { name: "Docs ", link: "#Docs" },
        { name: "Pricing ", link: '/pricing' },
        
        { name: "Sign in ", link: "#Sign in" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},
    ];
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
        ? " py-4 bg-slate-950 border-violet-950"
        : " py-6 bg-transparent border-transparent")}
>
<div>
    <a href="http://localhost:5173/" class="button">Resend</a>
    
</div>
   
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <!-- <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-violet-600 text-white"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Login</h4>
        </button> -->
        <button
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-3 py-3 group rounded-full bg-white text-slate-950"
      >
        <div
          class=" top-0 right-full w-full h-full  group-hover:translate-x-full"
        />
        <a href="https://resend.com/signup" class="button">Get Started</a>
      </button>
        </div>
    
</header>
