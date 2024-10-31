<script lang="ts">
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
    <internships class="mx-auto mt-28 grid place-items-center w-11/12">
        <h1 class="text-rose-400 self-center text-5xl font-bold mb-1">
            Here are some of the companies I have worked for!
        </h1>
        <companyList class="flex mt-10 w-9/12 border">
            <InterestItem title="Abercrombie & Fitch"/>
            <InterestItem title="Protiviti"/>
            <InterestItem title="Cognosos"/>
            <InterestItem title="Carvana"/>
        </companyList>
    </internships>
    <projects class="mx-auto mt-28 grid place-items-center w-11/12">
        <h1 class="text-rose-400 self-center text-5xl font-bold mb-1">
            Here are some of the projects I have worked on
        </h1>
        <projectsList class="flex border">
            <InterestItem title="Neovim/Tmux"/>
            <InterestItem title="Golang"/>
            <InterestItem title="Real Time Systems and Music Tech"/>
            <InterestItem title="The Juce Framework"/>
        </projectsList></projects
    >

    <toolsILike class="mx-auto mt-28 grid place-items-center w-11/12"
        ><h1 class="text-rose-400 self-center text-5xl font-bold mb-1">
            Here are some tools & technologies that I really like
        </h1>
        <toolsList class="flex border">
            <InterestItem title="Guitar Effects Pedal"/>
            <InterestItem title="Instrument Classification Neural Network"/>
            <InterestItem title="EpiInfo CDC Application"/>
            <InterestItem title="Hardware Servo Motor Controller"/>
            >
        </toolsList></toolsILike
    >
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
