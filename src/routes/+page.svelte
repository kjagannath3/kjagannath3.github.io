<script lang="ts">
    import { AccordionItem, Accordion } from "flowbite-svelte";
    import Navbar from "$lib/Navbar.svelte";
    import InterestItem from "$lib/InterestItem.svelte";
    let name: string = "";
    let email: string = "";
    let content: string = "";
    function getContent() {
        console.log(name == "" ? "No name yet" : name);
        console.log(email == "" ? "No email yet" : email);
        console.log(content == "" ? "No content yet" : content);
    }
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
    <internshipList class="grid place-items-center justify-center">
        <h1 class="text-5xl font-bold text-rose-400">
            Take a look at some of the companies I have applied to!
        </h1>
        <Accordion>
            <AccordionItem>
                <span slot="header">Abercrombie & Fitch</span>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="text-gray-500 dark:text-gray-400">
                    Check out this guide to learn how to <a
                        href="/"
                        target="_blank"
                        rel="noreferrer"
                        class="text-blue-600 dark:text-blue-500 hover:underline"
                    >
                        get started
                    </a>
                    and start developing websites even faster with components on
                    top of Tailwind CSS.
                </p>
            </AccordionItem>
            <AccordionItem>
                <span slot="header">Cognosos</span>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Learn more about these technologies:
                </p>
                <ul class="list-disc ps-5 dark:text-gray-400 text-gray-500">
                    <li>
                        <a
                            href="/"
                            target="_blank"
                            rel="noreferrer"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Lorem ipsum
                        </a>
                    </li>
                    <li>
                        <a
                            href="https://tailwindui.com/"
                            rel="noreferrer"
                            target="_blank"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Tailwind UI
                        </a>
                    </li>
                </ul>
            </AccordionItem>
            <AccordionItem>
                <span slot="header">Protiviti</span>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Learn more about these technologies:
                </p>
                <ul class="list-disc ps-5 dark:text-gray-400 text-gray-500">
                    <li>
                        <a
                            href="/"
                            target="_blank"
                            rel="noreferrer"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Lorem ipsum
                        </a>
                    </li>
                    <li>
                        <a
                            href="https://tailwindui.com/"
                            rel="noreferrer"
                            target="_blank"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Tailwind UI
                        </a>
                    </li>
                </ul>
            </AccordionItem>
            <AccordionItem >
                <span slot="header">Carvana</span>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Illo ab necessitatibus sint explicabo ...
                </p>
                <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Learn more about these technologies:
                </p>
                <ul class="list-disc ps-5 dark:text-gray-400 text-gray-500">
                    <li>
                        <a
                            href="/"
                            target="_blank"
                            rel="noreferrer"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Lorem ipsum
                        </a>
                    </li>
                    <li>
                        <a
                            href="https://tailwindui.com/"
                            rel="noreferrer"
                            target="_blank"
                            class="text-blue-600 dark:text-blue-500 hover:underline"
                        >
                            Tailwind UI
                        </a>
                    </li>
                </ul>
            </AccordionItem>
        </Accordion>
    </internshipList>

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
