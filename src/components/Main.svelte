<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Dogspotter",
            icon: "fa-solid fa-shield-dog",
            href: "https://github.com/rollinsals/dogspotter",
        },
        {
            name: "Lending Library",
            icon: "fa-solid fa-book",
            href: "https://github.com/rollinsals/library-in-flask",
        },
        {
            name: "Fen Friends",
            icon: "fa-solid fa-spaghetti-monster-flying",
            href: "https://salsberyr.itch.io/fen-friends",
        },
    ];

    let benefits = [
        {
            name: "(Mostly) Self-Taught Developer",
            description:
                "Driven to bring to life my own video game vision, I taught myself the basics of code and game development in engines like Unity and Pico-8. I've since expanded further with an intensive bootcamp through Nucamp to polish up my skills.",
        },
        {
            name: "Data-Driven with an Eye for Design",
            description:
                "My previous work has been in merchandising for online retail - merging detailed sales analysis with aesthetic decision-making and a comprehensive tech stack.",
        },
        {
            name: "Consistent, Dedicated, and Adaptable",
            description:
                "Whatever the job throws at me, I'm ready to learn, shift, and fill the needs",
        },
    ];
</script>

<main class="flex flex-1 flex-col p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 gap-10 py-8 sm:py-14 lg:grid-cols-2"
    >
        <div
            class="flex flex-col gap-6 text-center md:gap-8 lg:justify-center lg:gap-10 lg:text-left"
        >
            <h2 class="text-4xl font-semibold sm:text-5xl md:text-6xl">
                Hi, I'm <span class="playfair text-teal-600">Rollin</span>
                Salsbery <br /> Backend & Game
                <span class="playfair text-teal-600"> Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-lg">
                Working with Django, Flask, PostgreSQL, SvelteKit, & TailwindCSS
            </p>
            <a
                href="mailto:salsberyr@gmail.com"
                target="_blank"
                class="blueShadow playfair group relative mx-auto cursor-pointer overflow-hidden rounded-full bg-white px-6 py-3 text-base text-slate-950 sm:text-lg md:text-xl lg:ml-0 lg:mr-auto"
            >
                <div
                    class="absolute right-full top-0 z-0 h-full w-full bg-teal-500 opacity-20 duration-200 group-hover:translate-x-full"
                ></div>
                <h4 class="z-9 relative">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center shadow-2xl">
            <img
                src={"images/headshot.jpg"}
                alt="Profile Picture of Rollin"
                class="z-[2] max-h-[70vh] object-cover"
            />
        </div>
    </section>
    <section id="projects" class="flex flex-col gap-24 py-20 lg:py-32">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">The Projects Roster</h6>
            <h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
                Curious to <span class="playfair text-teal-600">see</span> my work?
            </h3>
        </div>
        <div class="lg:gap-18 grid grid-cols-1 gap-12 lg:grid-cols-3">
            <Step step={steps[0]}>
                <p>
                    Check-in style app for seeing dogs on the street Using <strong
                        class="text-teal-500">Django</strong
                    >
                    and <strong class="text-teal-500">PostgreSQL</strong> in a dockerized
                    environment
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    A lending library app backend. Built with <strong
                        class="text-teal-500">Flask</strong
                    >
                    and <strong class="text-teal-500">PostgreSQL</strong> for a RESTful
                    API
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    A Pico-8 micro adventure game. Written in <strong
                        class="text-teal-500">Lua</strong
                    > with strict constraints
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="relative flex flex-col gap-16 py-20 pt-10 sm:gap-20 md:gap-24 lg:py-32 lg:pt-16"
    >
        <div
            class="relative flex flex-col gap-2 py-4 text-center before:absolute before:left-0 before:top-0 before:h-1.5 before:w-2/3 before:bg-teal-700 after:absolute after:bottom-0 after:right-0 after:h-1.5 after:w-2/3 after:bg-teal-700"
        >
            <h6 class="text-lg sm:text-xl md:text-2xl">Still want more?</h6>
            <h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
                A bit <span class="playfair text-teal-400">about</span> me
            </h3>
        </div>
        <p
            class="playfair mx-auto text-lg font-semibold sm:text-xl md:text-2xl"
        >
            A Quick Bio
        </p>
        <div class="mx-auto flex w-full max-w-[800px] flex-col gap-20">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="playfair text-4xl font-semibold text-slate-500 sm:text-5xl md:text-6xl"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>
