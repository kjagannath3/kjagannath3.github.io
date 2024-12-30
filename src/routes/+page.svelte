<script lang="ts">
    import Accordion from "$lib/Accordion.svelte";
    import AccordionElement from "$lib/AccordionElement.svelte";
    import Navbar from "$lib/Navbar.svelte";
    
    interface IAccordionElement {
        title: string;
        blurb: string;
        imgPath?: string;  // Optional because projects don't have images
        visible?: boolean;  // Optional for accordion state
    }
    
    let companiesList: Array<IAccordionElement> = [
        {
            "title": "Abercrombie & Fitch",
            "blurb": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nunc id aliquam tincidunt, nisl nunc tincidunt nisi, vitae aliquam eros dolor vitae erat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices.",
            "imgPath": "abercrombie.png"
        },

        {
            "title": "Cognosos",
            "blurb": "Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
            "imgPath": "cognosos.png"
        },

        {
            "title": "Protiviti",
            "blurb": "Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt.",
            "imgPath": "protiviti.png"
        },

        {
            "title": "Carvana",
            "blurb": "Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea.",
            "imgPath": "carvana.png"
        }
    ]
    let projectsList: Array<IAccordionElement> = [
        {
            "title": "Instrument Classification Neural Network",
            "blurb": "Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus."
        },

        {
            "title": "FPGA morse code guessing game",
            "blurb": "Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur."
        },

        {
            "title": "EpiInfo Application",
            "blurb": "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam."
        },

        {
            "title": "Guitar Distortion Pedal",
            "blurb": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate."
        }
    ]

    
</script>

<body class="bg-gray-50">
    <topbar class="w-full mb-20">
        <Navbar />
    </topbar>
    <imagetitle class="mx-auto mt-28 grid place-items-center w-10/12">
        <h1 class="text-rose-400 self-center text-8xl font-bold mb-1">
            Hi, I'm Keshav!
        </h1>
        <content class="flex justify-around border">
            <textContent class="text-2xl my-36 w-1/2">
                <p class="w-full leading-10">
                    Glad you could make it! I am a senior computer science
                    student at Georgia Institute of Technology. I am interested
                    in backend development, IOT, music tech, and cloud
                    applications. I am currently looking for full time roles
                    with a graduation target of this December. Let's connect!
                </p>
            </textContent>
            <div>
                <img
                    class="w-[250px] my-24 h-auto rounded-full ml-0"
                    alt=""
                    src="keshav-jagannath-headshot.jpg"
                />
            </div>
        </content>
    </imagetitle>
    <internshipList class="grid place-items-center">
        <h1 class="text-5xl font-bold text-rose-400">
            Take a look at some of the companies I have applied to!
        </h1>
        <Accordion accordionElements={companiesList} />
    </internshipList>
    <projectsList class="grid place-items-center  ">
        <h1 class="text-5xl font-bold text-rose-400">
            Take a look at some of the projects I have completed!
        </h1>
        <Accordion accordionElements={projectsList}/>
    </projectsList>
    <callToAction class="mx-auto mt-64 grid place-items-center">
        <h3 class="text-5xl font-bold text-rose-400">Let's get in touch!</h3>
        <a
            class="my-5 mb-96 text-2xl font-bold text-blue-800 duration-150 hover:text-rose-400"
            href="mailto:keshavjagannath123@gmail.com"
        >
            Send me an email!</a
        >
    </callToAction>
</body>
