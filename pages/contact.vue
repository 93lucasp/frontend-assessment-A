<template>
    <section class=" mt-20">
        <div class="container space-y-[86px]">
            <div class="text-center space-y-9">
                <h1 class="text-center text-4xl md:text-7xl text-white">
                    <span class="font-medium italic">
                        NEXT LEVEL PADEL
                    </span> <br>
                    CONTRIBUISCI CON IL TUO CLUB <br>
                    ALLA <span class="italic font-medium">RIVOLUZIONE</span>
                </h1>
                <p class="text-white text-xl md:text-2xl">
                    Contattaci per maggiori informazioni o per candidare il tuo Club. <br>
                    Utilizza il modulo sottostante o inviaci una e-mail a <span
                        class=" text-secondary">info@padeldao.com</span>
                </p>
            </div>
            <div class="">
                <form @submit="storeContactInfo" class="max-w-[639px] mx-auto">
                    <div class="space-y-9">
                        <form-input input-type="text" id="name" input-placeholder="Inserisci il nome"
                            input-label="Nome del tuo Club" v-model="formContact.clubName" />
                        <form-input input-type="text" id="vat" input-placeholder="Inserisci la P.IVA"
                            input-label="P.IVA/VAT" v-model="formContact.vat" />
                        <form-input input-type="email" id="email" input-placeholder="Indirizzo email"
                            input-label="E-mail" v-model="formContact.email" />
                        <form-input input-type="text" id="club-city" input-placeholder="Città"
                            input-label="In quale città si trova il tuo Club?" v-model="formContact.clubCity" />
                        <div>
                            <button type="submit" class="btn-primary w-full">Invia la candidatura</button>
                        </div>
                    </div>
                </form>
                <div class="text-lg text-white text-center mt-11">
                    Cliccando su "Invia la candidatura", accetti la nostra <nuxt-link to="/"
                        class="text-secondary hover:text-secondary/80">
                        Privacy Policy
                    </nuxt-link> e consenti a <br> PadelDao di utilizzare queste informazioni per scopi di marketing.
                </div>
            </div>
        </div>
        <div class="container mt-[105px]">
            <div class="bg-[#D3E2E8] py-12 flex items-center">
                <img src="/contact-cta.png" alt="contact cta" class="p-0 hidden xl:inline" />
                <div class="pl-8 xl:pl-[97px] pr-4 xl:max-w-[594px]">
                    <h6 class=" text-3xl text-app-bg font-medium">PadelDao Pitch</h6>
                    <p class=" text-2xl font-medium text-[#4D696D] mt-5">
                        Vuoi scoprire di più su di noi? Qui potrai esplorare il nostro progetto, scoprire
                        la nostra mission e vision, capire perché
                        per unirti a noi e conoscere le soluzioni
                        che proponiamo ai problemi più diffusi. Approfondirai i dettagli delle nostre membership card
                        NFT e i servizi unici
                        che offriamo.
                    </p>
                    <div class="mt-7">
                        <button class="btn-secondary">Downlaod pitch</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
// state
const formContact = reactive({
    clubName: '',
    email: '',
    vat: '',
    clubCity: ''
})

// methods
function storeContactInfo(e) {
    e.preventDefault();
    alert(JSON.stringify(formContact))
}
</script>
