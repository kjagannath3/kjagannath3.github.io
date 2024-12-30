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
            "blurb": "This is the abercrombie and fitch blurb",
            "imgPath": "abercrombie.png"
        },

        {
            "title": "Cognosos",
            "blurb": "This is the Cognosos blurb",
            "imgPath": "cognosos.png"
        },

        {
            "title": "Protiviti",
            "blurb": "This is the Protiviti blurb",
            "imgPath": "protiviti.png"
        },

        {
            "title": "Carvana",
            "blurb": "This is the Carvana blurb",
            "imgPath": "carvana.png"
        }
    ]
    let projectsList: Array<IAccordionElement> = [
        {
            "title": "Instrument Classification Neural Network",
            "blurb": "This is the instrument classification neural network blurb"
        },

        {
            "title": "FPGA morse code guessing game",
            "blurb": "This is the morse codee guessing game blurb"
        },

        {
            "title": "EpiInfo Application",
            "blurb": "This is the EpiInfo Application blurb"
        },

        {
            "title": "Guitar Distortion Pedal",
            "blurb": "This is the Guitar Distortion Pedal blurb"
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
