<script lang="ts">
    import Navbar from "$lib/Navbar.svelte";
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
<topbar class="w-full">
    <Navbar />
</topbar>
<imagetitle class="mx-auto mt-28 grid place-items-center w-10/12">
    <h1 class="text-red-400 self-center text-3xl font-bold">Hi, I'm Keshav!</h1>
    <content class="flex justify-around border">
        <textContent class="mt-24 ml-3 w-1/4">
            <p>
                Glad you could make it! I am a senior computer science student
                at Georgia Institute of Technology. I am interested in backend
                development, IOT, music tech, and cloud applications. I am
                currently looking for full time roles with a graduation target
                of this December. Let's connect!
            </p>
        </textContent>
        <div>
            <img
                class="w-[300px] h-auto rounded-full ml-auto"
                alt=""
                src="keshav-jagannath-headshot.jpg"
            />
        </div>
    </content>
</imagetitle>
<callToAction class="mx-auto mt-24 grid place-items-center">
    <h3 class="text-3xl font-bold">Let's get in touch!</h3>
        <a class="my-5" href="mailto:keshavjagannath123@gmail.com"> Send me an email!</a>
</callToAction>
</body>
