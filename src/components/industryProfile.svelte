<script>
    import ajak from '../assets/ajakonline-logo.png'
</script>


    <div class={`grid grid-cols-1 place-items-center overflow-hidden ${$$props.class}`}>
        <slot/>

        <div class="font-bold text-2xl mt-7">PROFIL PERUSAHAAN</div>

        <div class="container mt-7 text-center text-white rounded-xl w-[80%] px-3 bg-gradient-to-tl from-[#00ffaa] via-[#0000ff] via-40% to-[#00ddee] to-95% shadow-[40px] none">
            <div class="font-bold text-lg my-5">Ajak Online</div>
            <img src="{ajak}" alt="" class="w-[85%] rounded-xl mx-auto">
            <div class="container text-left text-base w-[90%] my-3 mx-auto">
                <h4 class="mt-4">Nama Pimpinan : Wahyu Lulianto</h4>
                <h4 class="mt-2">No. Telepon : 085226355566</h4>
                <h4 class="mt-2">Website : ajakonline.com</h4>
                <h4 class="mt-2">Alamat : Jl. Bromo Raya No.88, Geplukan, Kadipiro, Banjarsari, Surakarta</h4>
                <h4 class="mt-2">Bidang : Jasa Pembuatan Website</h4>
            </div>
        </div>

        <div class="desc container w-[90%] rounded-xl mx-auto my-10 p-4 text-white text-xl text-center">
            Ajakonline merupakan ahli jasa pembuatan website, menawarkan solusi digital inovatif dan profesional. Dengan tim desainer kreatif dan pengembang web handal, Ajakonline fokus pada menciptakan situs web yang tidak hanya estetis, tetapi juga fungsional. 
        </div>
    </div>

    <style>
        .desc{
            background: #00ffaa;
            background: radial-gradient(at left bottom, #00ffaa -10%, #0000FF);
        }
    </style>



