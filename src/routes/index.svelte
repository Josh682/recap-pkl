<script>
    import Test from '../components/tes.svelte'
    import Grid from '../components/contentGrid.svelte'
    import hero from '../assets/hero.jpeg'
    import profile from '../assets/profile-img.jpeg'
    import teams from '../assets/team-profile.jpeg'
    import ajak from '../assets/ajakonline-logo.png'
    import timeline from '../assets/timeline.jpeg'
</script>

<div class="bg"></div>
<div class="container mx-auto h-[100vh]">

    <div class="head border border-white rounded-2xl w-[90%] mx-auto mt-5 grid grid-cols-[60%_auto] py-2">
        <div class="grid grid-cols-1 text-white">
            <span class="ml-3 text-xl font-bold">Hello! I'm Joshua </span>
            <span class="ml-3 text-[12.5px]">And this is my internship journey</span>

            <div class="ml-3 mt-7 grid grid-cols-3 gap-2 w-[50%]">
                <div class="border w-[20px] h-[20px] rounded-md"></div>
                <div class="border w-[20px] h-[20px] rounded-md"></div>
                <div class="border w-[20px] h-[20px] rounded-md"></div>
            </div>
        </div>
        <div class="grid grid-cols-1 place-items-center">
            <div class="img w-[100px] h-[100px] rounded-full border border-white">
                <img src="{hero}" alt="" class="rounded-full">
            </div>
        </div>
    </div>

    <h3 class="mt-2 text-center text-lg text-white font-bold">Profile</h3>
    <div class="flex flex-row justify-evenly mx-auto mt-2 text-sm">
        <div class="grid grid-cols-1 place-items-center">
            <img src="{profile}" alt="" class="rounded-xl w-[70px] h-[70px]">
            <h4 class="text-white font-bold text-center">Joshua</h4>
        </div>
        <div class="grid grid-cols-1 place-items-center">
            <img src="{ajak}" alt="" class="rounded-xl w-[70px] h-[70px]">
            <h4 class="text-white font-bold text-center">AjakOnline</h4>
        </div>
        <div class="grid grid-cols-1 place-items-center">
            <img src="{teams}" alt="" class="rounded-xl w-[70px] h-[70px]">
            <h4 class="text-white font-bold text-center">Teams</h4>
        </div>
    </div>
    <h2 class="font-bold text-2xl text-center mt-12">Content</h2>
    <div class="grid grid-cols-1 place-items-center mt-5 gap-4 text-lg">
        <Grid>
            <Test>
                <img src="{timeline}" alt="" class="w-full h-full rounded-xl">
            </Test>
            <h3 class="mt-2">Timeline</h3>
        </Grid>
        <Grid>
            <Test/>
            <h3 class="mt-2">Projects</h3>
        </Grid>
        <Grid>
            <Test/>
            <h3 class="mt-2">Moments</h3>
        </Grid>
    </div>
    <!-- <div class="grid grid-cols-2 mt-5">
        <div class="grid grid-cols-1 place-items-center">
            <div class="h-[345px] w-[150px] border border-black ">

            </div>
            <h3 class="text-xl font-bold mt-3">Timeline</h3>
        </div>
        <div class="a">
            <div class="grid grid-cols-1 place-items-center">
                <div class="h-[150px] w-[150px] border border-black ">
    
                </div>
                <h3 class="text-xl font-bold my-2">Projects</h3>
            </div>
            <div class="grid grid-cols-1 place-items-center">
                <div class="h-[150px] w-[150px] border border-black ">  
    
                </div>
                <h3 class="text-xl font-bold mt-2">Moments</h3>
            </div>
        </div>
    </div> -->
</div>

<style lang="scss">

        $grad: linear-gradient(to top left, #00ffc8, blue);
        $clip: circle(50% at 50% 0%);
    
    .bg{
        height: 100vh;
        width: 100%;
        background-image: $grad;
        clip-path: $clip;
    }
    .container{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50% , -50%);
    }
</style>
