<script>
    export let y;
    let tabs = [
        { name: "Projects", link: "#projects" },
        { name: "About Me", link: "#about" },
    ];
</script>

<header
    class={"sticky top-0 z-[10] flex items-center justify-between border border-solid px-6 duration-200 " +
        (y > 0
            ? " border-teal-950 bg-slate-950 py-4"
            : " border-transparent bg-transparent py-6")}
>
    <h1 class="font-medium">Rollin Salsbery</h1>
    <div class="hidden items-center gap-4 sm:flex">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-teal-500">
                <p>{tab.name}</p>
            </a>
        {/each}

        <a
            href="#footer"
            class="blueShadow group relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950"
        >
            <div
                class="absolute right-full top-0 z-0 h-full w-full bg-teal-500 opacity-60 duration-200 group-hover:translate-x-full"
            ></div>
            <h4 class="z-9 relative">Get in touch</h4>
        </a>
    </div>
</header>
