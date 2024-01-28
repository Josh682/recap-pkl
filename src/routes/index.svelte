<script lang="ts">
    import '@fortawesome/fontawesome-free/css/all.min.css'

    import Grid from '../components/contentGrid.svelte'
    import Label from '../components/contentLabel.svelte'
    import Industry from '../components/industryProfile.svelte'
    import Team from '../components/teamProfile.svelte'

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
            
            <div class="grid grid-cols-1 place-items-center overflow-hidden">
                <div class="font-bold text-2xl mt-5">PROFIL TEAM</div>

                <Team>
                    <div class="font-bold text-2xl mt-5">Joshua</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Joshua Satria Kusuma</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Surakarta, 25 November 2006</h4>
                        <h4 class="mt-2">Alamat : Dempo Serut Rt. 09 Rw. 12 Mojosongo, Jebres, Surakarta</h4>
                        <h4 class="mt-2">No. Telepon : 081227102119</h4>
                        <h4 class="mt-2">Website : joshuaskusuma.my.id</h4>
                    </div>  
                </Team>
                <Team>
                    <div class="font-bold text-2xl mt-5">Rangga</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Muhammad Rangga Prasetya</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Boyolali, 13 November 2005</h4>
                        <h4 class="mt-2">Alamat : Pilangsari RT05/RT01 Potronayan, Nogosari, Boyolali </h4>
                        <h4 class="mt-2">No. Telepon : 085163680621</h4>
                        <h4 class="mt-2">Website : ranggaprass.my.id</h4>
                    </div>  
                </Team>
                <Team>
                    <div class="font-bold text-2xl mt-5">Fano</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Stefano Talenta Putra</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Surakarta, 6 April 2006</h4>
                        <h4 class="mt-2">Alamat : Perumahan Puri Mandiri blok C12, Wonorejo, Gondangrejo, Karanganyar</h4>
                        <h4 class="mt-2">No. Telepon : 082221245234</h4>
                        <h4 class="mt-2">Website : stefanotalentap.my.id</h4>
                    </div>  
                </Team>
                <Team>
                    <div class="font-bold text-2xl mt-5">Lucas</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Lucas Christian Firdaus</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Karanganyar, 31 mei 2006</h4>
                        <h4 class="mt-2">Alamat : Ingasrejo rt02/08, Plesungan, Gondangrejo, Karanganyar.</h4>
                        <h4 class="mt-2">No. Telepon :  083159464322</h4>
                        <h4 class="mt-2">Website : lucasc.my.id</h4>
                    </div>  
                </Team>
                <Team>
                    <div class="font-bold text-2xl mt-5">Syafiq</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Muhammad Syafiq Shidiq</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Surakarta, 10 Februari 2006</h4>
                        <h4 class="mt-2">Alamat : Talang RT 7 RW 1, Banaran, Grogol, Sukoharjo</h4>
                        <h4 class="mt-2">No. Telepon : 089676025902</h4>
                        <h4 class="mt-2">Website : syafiqshidiq.my.id</h4>
                    </div>  
                </Team>
                <Team>
                    <div class="font-bold text-2xl mt-5">Zacky</div>
                    <img src="" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                    <div class="text-left text-sm mb-5 ml-2">
                        <h4 class="mt-4">Nama Lengkap : Muhammad Zacky Fikry Ali</h4>
                        <h4 class="mt-2">Tempat, Tgl Lahir : Surakarta, 18 Juli 2005</h4>
                        <h4 class="mt-2">Alamat : jl. Kacer 5 no.8 Manahan, Banjarsari, Surakarta</h4>
                        <h4 class="mt-2">No. Telepon : 081353716585</h4>
                        <h4 class="mt-2">Website : fikry.my.id</h4>
                    </div>  
                </Team>
            </div>

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