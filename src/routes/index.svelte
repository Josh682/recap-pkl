<script>
    import '@fortawesome/fontawesome-free/css/all.min.css'

    import Grid from '../components/contentGrid.svelte'
    import Label from '../components/contentLabel.svelte'
    import Industry from '../components/industryProfile.svelte'

    import hero from '../assets/hero.jpeg'
    import profile from '../assets/profile.png'
    import teams from '../assets/teams.png'
    import ajak from '../assets/ajakonline-logo.png'
</script>

<div class="all">
    <div class="container top mx-auto py-4 fixed top-0 bg-[#d8fff7] h-[300px]">
        <div class="head border border-white rounded-2xl w-[90%] mx-auto grid grid-cols-[60%_auto] py-4 ">
            <div class="grid grid-cols-1 text-white">
                <span class="ml-3 text-xl font-bold">Hello! I'm Joshua </span>
                <span class="ml-3 text-[12.5px]">And this is my internship journey</span>
    
                <div class="ml-3 mt-7 grid grid-cols-3 gap-2 w-[50%]">
                    <i class="fa-brands fa-instagram text-[25px]"></i>
                    <i class="fa-brands fa-whatsapp text-[25px]"></i>
                    <i class="fa-brands fa-github text-[25px]"></i>
                </div>
            </div>
            <Grid>
                <div class=" w-[100px] h-[100px] rounded-full">
                    <img src="{hero}" alt="" class="rounded-full w-full h-full">
                </div>
            </Grid>
        </div>
        <div class="flex flex-row justify-evenly mx-auto mt-5 text-sm">
            <Grid>
                <img src="{ajak}" alt="" class="rounded-xl w-[65px] h-[65px]">
                <Label class="mt-1">Industry</Label>
                <Label class="mt-[-3px]">Profile</Label>
            </Grid>
            <Grid>
                <img src="{teams}" alt="" class="rounded-xl w-[65px] h-[65px]">
                <Label class="mt-1">Team</Label>
                <Label class="mt-[-3px]">Profile</Label>
            </Grid>
            <Grid>
                <img src="{profile}" alt="" class="rounded-xl w-[65px] h-[65px]">
                <Label class="mt-1">Internship</Label>
                <Label class="mt-[-3px]">Story</Label>
            </Grid>
        </div>
    </div>
    <Industry class="mt-[300px]"/>
</div>



<style lang="scss">
    $grad: linear-gradient(to top left, #00ffc8, #0000ff);
    $clip: circle(50% at 50% 0%);

    .head{
        background-image: $grad;
    }
    .all{
        background-color: #d8fff7;
    }

</style>
