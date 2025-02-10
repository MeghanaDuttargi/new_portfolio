<script>
    export let y;

    export let tabs = [
        { name: "Projects", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Resume", link: "https://heyzine.com/flip-book/a752eaa2ea.html" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},
    ];

    // Function to open the mailto link
    function sendEmail() {
        window.open('mailto:meghana.msismpl2024@learner.manipal.edu', '_blank');
    }
</script>

<header
    class={"static z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <b class="font-bold poppins">Meghana D Duttargi</b> <span class=""></span>
    </h1>
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
        <button 
        on:click={sendEmail} 
        class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-violet-400 text-white"
    >
        <div 
            class="absolute top-0 right-full w-full h-full bg-violet-600 opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-10">Get in touch</h4>
    </button>
    
    </div>
</header>
