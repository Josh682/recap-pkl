<script>
    import ajak from '../assets/ajakonline-logo.png'
</script>


    <div class={`grid grid-cols-1 place-items-center overflow-hidden ${$$props.class}`}>
        <slot/>

        <div class="font-bold text-7xl mt-16">PROFIL PERUSAHAAN</div>

        <div class="container mt-16 text-center text-white rounded-[70px] w-[80%] px-3 bg-gradient-to-tl from-[#00ffaa] via-[#0000ff] via-40% to-[#00ddee] to-95% shadow-[40px] none">
            <div class="font-bold text-6xl my-10">Ajak Online</div>
            <img src="{ajak}" alt="" class="w-[60%] rounded-[60px] mt-4 mx-auto">
            <div class="text-left text-4xl ml-16 my-14">
                <h4 class="mt-10">Nama Pimpinan : Wahyu Lulianto</h4>
                <h4 class="mt-8">No. Telepon : 085226355566</h4>
                <h4 class="mt-8">Website : ajakonline.com</h4>
                <h4 class="mt-8">Alamat : Jl. Bromo Raya No.88, Geplukan, Kadipiro, Banjarsari, Surakarta</h4>
                <h4 class="mt-8">Bidang : Jasa Pembuatan Website</h4>
            </div>
        </div>

        <div class="desc container w-[90%] rounded-[30px] mx-auto my-20 p-4 text-white text-5xl text-center">
            Ajakonline merupakan ahli jasa pembuatan website, menawarkan solusi digital inovatif dan profesional. Dengan tim desainer kreatif dan pengembang web handal, Ajakonline fokus pada menciptakan situs web yang tidak hanya estetis, tetapi juga fungsional. 
        </div>
    </div>

    <style>
        .desc{
            background: #00ffaa;
            background: radial-gradient(at left bottom, #00ffaa -10%, #0000FF);
        }
    </style>



