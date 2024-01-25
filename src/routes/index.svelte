<script lang="ts">
    import '@fortawesome/fontawesome-free/css/all.min.css'

    import Grid from '../components/contentGrid.svelte'
    import Label from '../components/contentLabel.svelte'
    import Industry from '../components/industryProfile.svelte'

    import hero from '../assets/hero.jpeg'
    import profile from '../assets/profile.png'
    import teams from '../assets/teams.png'
    import ajak from '../assets/ajakonline-logo.png'

    function openTab(tabName: string) {
        
    const tabContents = document.querySelectorAll('.tab-content') as NodeListOf<HTMLElement>;
    tabContents.forEach(content => {
        content.classList.remove('show');
    });

    const tabs = document.querySelectorAll('button') as NodeListOf<HTMLButtonElement>;
    tabs.forEach(tab => {
        tab.classList.remove('active');
    });

    const selectedTabContent = document.getElementById(tabName);
    if (selectedTabContent) {
        selectedTabContent.classList.add('show');
    }

    const selectedTab = document.getElementById('tab' + tabName.slice(-1));
    if (selectedTab) {
        selectedTab.classList.add('active');
    }
}

openTab('industry');

</script>

<div class="all">
    <div class="container top mx-auto py-4 fixed top-0 bg-[#d8fff7] h-[280px]">
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
            <button id="tab1" on:click={()=> openTab('industry')}>
                <Grid>
                    <img src="{ajak}" alt="" class="rounded-xl w-[65px] h-[65px]">
                    <Label class="mt-1">Industry</Label>    
                </Grid>
            </button>
            <button id="tab2" on:click={()=> openTab('team')}>
                <Grid>
                    <img src="{teams}" alt="" class="rounded-xl w-[65px] h-[65px]">
                    <Label class="mt-1">Team</Label>
                </Grid>
            </button>
            <button id="tab3" on:click={()=> openTab('story')}>
                <Grid>
                    <img src="{profile}" alt="" class="rounded-xl w-[65px] h-[65px]">
                    <Label class="mt-1">Story</Label>
                </Grid>
            </button>
        </div>
    </div>

    <div class="bot mt-[280px] rounded-3xl bg-white shadow-[35px_#000000] flex">
        <div class="tab-content show" id="industry">
            <Industry/>
        </div>
        <div class="tab-content" id="team">
            <Industry>
                <h1 class="text-center text-2xl">TEAM</h1>
            </Industry>
        </div>
        <div class="tab-content" id="story">
            <Industry>
                <h1 class="text-center text-2xl">Story</h1>
            </Industry>
        </div>
    </div>
    
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
    .tab-content {
        display: none;
    }
    .tab-content.show{
        display: block;
    }
</style>