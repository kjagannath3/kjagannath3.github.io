<script lang="ts">
    import Accordion from "$lib/Accordion.svelte";
    import AccordionElement from "$lib/AccordionElement.svelte";
    import Navbar from "$lib/Navbar.svelte";
    import InterestItem from "$lib/InterestItem.svelte";
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
                    src="grad_photo.jpg"
                />
            </div>
        </content>
    </imagetitle>
    <h1 class="font-bold text-center text-3xl pb-10">Take a look at some of the internships I've completed!</h1>
    <internshipList
        class=" flex flex-wrap justify-center items-center w-10/12 mx-auto h-screen self-center"
    >
        <InterestItem title="Abercrombie & Fitch" imagePath="abercrombie.png" />
        <InterestItem title="Protiviti" />
        <InterestItem title="Cognosos" />
        <InterestItem title="Carvana" />
    </internshipList>
</body>
