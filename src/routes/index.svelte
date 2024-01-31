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
    import jojo from '../assets/jojo.jpeg'
    import fano from '../assets/fano.jpeg'
    import rangga from '../assets/rangga.jpeg'
    import lucas from '../assets/lucas.jpeg'
    import syafiq from '../assets/syafiq.jpeg'
    import fikry from '../assets/fikry.jpeg'
    import josan from '../assets/josan.png'
    import portfolio from '../assets/portfolio.png'
    import sekolah from '../assets/sekolah.png'

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

openTab('project');

</script>

<div class="all">
    <div class="py-5 fixegd top-0 bg-[#c8fff4] h-[250px] w-[100vw]">
        <div class="head border border-white rounded-xl w-[90%] mx-auto grid grid-cols-[60%_auto]">
            <div class="grid grid-cols-1 text-white">
                <span class="ml-3 mt-5 text-lg font-bold">Hello! I'm Joshua </span>
                <span class="ml-3 mt-[-8px] text-base">And this is my internship journey</span>
    
                <div class="ml-3 mt-4 grid grid-cols-3 w-[50%]">
                    <a href="https://www.instagram.com/joshuask_/">
                        <i class="fa-brands fa-instagram text-[25px]"></i>
                    </a>
                    <a href="https://api.whatsapp.com/send/?phone=6281227102119&text&type=phone_number&app_absent=0">
                        <i class="fa-brands fa-whatsapp text-[25px]"></i>
                    </a>
                    <a href="https://github.com/Josh682">
                        <i class="fa-brands fa-github text-[25px]"></i>                    
                    </a>
                </div>
            </div>
            <Grid>
                <div class=" w-[100px] h-[100px] rounded-full my-5">
                    <img src="{hero}" alt="" class="rounded-full w-full h-full">
                </div>
            </Grid>
        </div>
        <div class="flex flex-row justify-between mx-auto mt-5 text-sm w-[90vw]">
            <button id="tab1" on:click={()=> openTab('industry')}>
                <Grid>
                    <img src="{ajak}" alt="" class="rounded-[15px] w-[50px] h-[50px]">
                    <Label>Industry</Label>    
                </Grid>
            </button>
            <button id="tab2" on:click={()=> openTab('team')}>
                <Grid>
                    <img src="{teams}" alt="" class="rounded-[15px] w-[50px] h-[50px]">
                    <Label>Team</Label>
                </Grid>
            </button>
            <button id="tab3" on:click={()=> openTab('project')}>
                <Grid>
                    <img src="{profile}" alt="" class="rounded-[15px] w-[50px] h-[50px]">
                    <Label>Projects</Label>
                </Grid>
            </button>
        </div>
    </div>

    <div class="bot mt-[300px] rounded-2xl bg-white shadow-[35px_#000000] flex justify-center align-middle">
        <div class="tab-content" id="industry">
            <Industry/>
        </div>
        <div class="tab-content" id="team">
            
            <Grid class="overflow-hidden">
                <div class="font-bold text-7xl my-16">PROFIL TEAM</div>

                <div class="grid grid-cols-2 place-items-center">
                    <Team>
                        <div class="font-bold text-5xl mt-5">Joshua</div>
                        <img src="{jojo}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Joshua Satria Kusuma</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Surakarta, 25 November 2006</h4>
                            <h4 class="mt-8">Alamat : Dempo Serut Rt. 09 Rw. 12 Mojosongo, Jebres, Surakarta</h4>
                            <h4 class="mt-8">No. Telepon : 081227102119</h4>
                            <h4 class="mt-8">Website : joshuaskusuma.my.id</h4>
                        </div>  
                    </Team>
                    <Team>
                        <div class="font-bold text-5xl mt-5">Rangga</div>
                        <img src="{rangga}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Muhammad Rangga Prasetya</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Boyolali, 13 November 2005</h4>
                            <h4 class="mt-8">Alamat : Pilangsari RT05/RT01 Potronayan, Nogosari, Boyolali </h4>
                            <h4 class="mt-8">No. Telepon : 085163680621</h4>
                            <h4 class="mt-8">Website : ranggaprass.my.id</h4>
                        </div>  
                    </Team>
                    <Team>
                        <div class="font-bold text-5xl mt-5">Fano</div>
                        <img src="{fano}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Stefano Talenta Putra</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Surakarta, 6 April 2006</h4>
                            <h4 class="mt-8">Alamat : Perumahan Puri Mandiri blok C12, Wonorejo, Gondangrejo, Karanganyar</h4>
                            <h4 class="mt-8">No. Telepon : 082221245234</h4>
                            <h4 class="mt-8">Website : stefanotalentap.my.id</h4>
                        </div>  
                    </Team>
                    <Team>
                        <div class="font-bold text-5xl mt-5">Lucas</div>
                        <img src="{lucas}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Lucas Christian Firdaus</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Karanganyar, 31 mei 2006</h4>
                            <h4 class="mt-8">Alamat : Ingasrejo rt02/08, Plesungan, Gondangrejo, Karanganyar.</h4>
                            <h4 class="mt-8">No. Telepon :  083159464322</h4>
                            <h4 class="mt-8">Website : lucasc.my.id</h4>
                        </div>  
                    </Team>
                    <Team>
                        <div class="font-bold text-5xl mt-5">Syafiq</div>
                        <img src="{syafiq}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Muhammad Syafiq Shidiq</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Surakarta, 10 Februari 2006</h4>
                            <h4 class="mt-8">Alamat : Talang RT 7 RW 1, Banaran, Grogol, Sukoharjo</h4>
                            <h4 class="mt-8">No. Telepon : 089676025902</h4>
                            <h4 class="mt-8">Website : syafiqshidiq.my.id</h4>
                        </div>  
                    </Team>
                    <Team>
                        <div class="font-bold text-5xl mt-5">Zacky</div>
                        <img src="{fikry}" alt="" class="w-[60%] rounded-2xl mt-4 mx-auto">
                        <div class="text-left text-3xl mb-5 ml-2">
                            <h4 class="mt-10">Nama Lengkap : Muhammad Zacky Fikry Ali</h4>
                            <h4 class="mt-8">Tempat, Tgl Lahir : Surakarta, 18 Juli 2005</h4>
                            <h4 class="mt-8">Alamat : jl. Kacer 5 no.8 Manahan, Banjarsari, Surakarta</h4>
                            <h4 class="mt-8">No. Telepon : 081353716585</h4>
                            <h4 class="mt-8">Website : fikry.my.id</h4>
                        </div>  
                    </Team>
                </div>
            </Grid>

        </div>
        <div class="tab-content show" id="project">
            <Grid>
                <Grid class="my-8">
                    <h2 class="text-2xl text-center font-bold mb-3">Website Portfolio</h2>
                    <img src="{portfolio}" alt="" class="w-[80%]">
                    <span class="text-base w-[80%] mt-3">Salah satu hasil produk saya selama magang di Ajak Online adalah website portfolio yang dibuat denga html, css, javascript, dan bootsrap, yang dihosting menggunakan github pages dan menggunakan custom domain .my.id</span>
                    <a href="joshuaskusuma.my.id" class="w-[80%] text-lg text-left text-blue-600 mt-3 underline">Lihat Disini</a>
                </Grid>
                <Grid class="my-8">
                    <h2 class="text-2xl text-center font-bold mb-3">Landing Page <br/> Website Sekolah</h2>
                    <img src="{sekolah}" alt="" class="w-[80%]">
                    <span class="text-base w-[80%] mt-3">Selain website portfolio pribadi yang bisa digunakan sebagai cv online, sya juga membuat template landing page sekolah yang bisa di export dalam bentuk file .json dan dijual secara komersil</span>
                </Grid>   
                <Grid class="my-8">
                    <h2 class="text-2xl text-center font-bold mb-3">Website Promosi <br/> Produk/Perusahaan</h2>
                    <img src="{josan}" alt="" class="w-[80%]">
                    <span class="text-base w-[80%] mt-3">Salah satu hasil produk saya selama magang di Ajak Online adalah website portfolio yang dibuat denga html, css, javascript, dan bootsrap, yang dihosting menggunakan github pages dan menggunakan custom domain .my.id</span>
                    <a href="batikjosan.com" class="w-[80%] text-lg text-left text-blue-600 mt-3 underline">Lihat Disini</a>
                </Grid>
            </Grid>     
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