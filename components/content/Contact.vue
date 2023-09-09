<template>
    

      <div class="relative bg-colorHeaderBgMenuPopupLight dark:bg-colorHeaderBgMenuPopupDark">
        <div class="lg:absolute lg:inset-0">
          <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
            <img class="h-56 w-full object-cover lg:absolute lg:h-full" src="https://images.unsplash.com/photo-1556761175-4b46a572b786?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80" alt="" />
          </div>
        </div>
        <div class="relative py-16 px-4 sm:py-24 sm:px-6 lg:mx-auto lg:grid lg:max-w-7xl lg:grid-cols-2 lg:px-8 lg:py-32">
          <div class="lg:pr-8">
            <div class="mx-auto max-w-md sm:max-w-lg lg:mx-0">
              <h2 class="text-3xl font-bold tracking-tight sm:text-4xl text-colorTxtLight dark:text-colorTxtDark">{{ t('title') }}</h2>
              <p class="mt-4 text-lg text-colorTxtLight dark:text-colorTxtDark sm:mt-3">{{ t('subtitle') }}</p>
              
              
              
              
              
              
                    <form action="https://kwesforms.com/api/foreign/forms/yHXyGSxCyxlT9BAJ1Hip" class="kwes-form grid grid-cols-1 gap-y-6 sm:grid-cols-1 sm:gap-x-8 mt-12" :lang="lang" no-reload>

        <div class="sm:col-span-2">
          <label for="first_name" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contactfirstname') }}</label>
          <div class="mt-1">
            <input type="text" name="first_name" id="first_name" autocomplete="given-name" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" rules="required|max:255">
          </div>
        </div>
        <div class="sm:col-span-2">
          <label for="last_name" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contactlastname') }}</label>
          <div class="mt-1">
            <input type="text" name="last_name" id="last_name" autocomplete="family-name" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" rules="required|max:255">
          </div>
        </div>
        <div class="sm:col-span-2">
          <label for="company" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contactcompany') }}</label>
          <div class="mt-1">
            <input type="text" name="company" id="company" autocomplete="organization" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" rules="required|max:255">
          </div>
        </div>
        <div class="sm:col-span-2">
          <label for="email" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contactemail') }}</label>
          <div class="mt-1">
            <input id="email" name="email" type="email" autocomplete="email" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" rules="required|max:255">
          </div>
        </div>
        <div class="sm:col-span-2">
          <label for="phone_number" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contacttel') }}</label>
          <div class="mt-1 relative rounded-md shadow-sm">
            <input type="text" name="phone_number" id="phone_number" autocomplete="tel" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" placeholder="+32 (123) 45 67 89" rules="required|max:255">
          </div>
        </div>
        <div class="sm:col-span-2">
          <label for="message" class="block text-sm font-medium text-gray-700 dark:text-white">{{ t('contactmessage') }}</label>
          <div class="mt-1">
            <textarea id="message" name="message" rows="4" class="py-3 px-4 block w-full shadow-sm focus:ring-indigo-500 focus:border-indigo-500 border-gray-300 rounded-md dark:text-gray-900" rules="required|max:255"></textarea>
          </div>
        </div>
        <div class="sm:col-span-2">
          <button type="submit" class="w-full inline-flex items-center justify-center px-6 py-3 border border-transparent rounded-md shadow-sm text-base font-medium text-black bg-yellow-400 hover:bg-yellow-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-yellow-500">
            {{ t('contactsend') }}
          </button>
        </div>
      </form>
              










            </div>
          </div>
        </div>
      </div>








      <!-- Contact grid -->
      <!-- <section aria-labelledby="offices-heading">
        <div class="mx-auto max-w-7xl py-24 px-4 sm:py-32 sm:px-6 lg:px-8">
          <h2 id="offices-heading" class="text-3xl font-bold tracking-tight text-colorTxtLight dark:text-colorTxtDark">{{ t('office') }}</h2>
          <div class="mt-10 grid grid-cols-1 gap-10 sm:grid-cols-2 lg:grid-cols-4">
            <div v-for="office in offices" :key="office.id">
              <h3 class="text-lg font-medium text-colorTxtLight dark:text-colorTxtDark">{{ office.city }}</h3>
              <p class="mt-2 text-base text-colorTxtLight dark:text-colorTxtDark">
                <span v-for="line in office.address" :key="line" class="block">{{ line }}</span>
              </p>
            </div>
          </div>
        </div>
      </section> -->









      <!-- CTA Section -->
      <!-- <div class="bg-gradient-to-r from-colorHighLight to-colorHoverHighLight dark:from-colorHighDark dark:to-colorHoverHighDark">
        <div class="mx-auto max-w-md py-16 px-4 text-center sm:max-w-2xl sm:py-24 sm:px-6 lg:px-8 lg:py-32">
          <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">
            <span class="block text-white">{{ t('hiretitle') }}</span>
            <span class="block text-colorTxtLight">{{ t('hiresubtitle') }}</span>
          </h2>
          <NuxtLink :to="localePath('/careers')" class="mt-8 inline-flex w-full items-center justify-center rounded-md border border-transparent bg-white py-3 px-5 text-base font-medium text-colorTxtDark shadow-md sm:w-auto">
            <span class="text-colorTxtLight">{{ t('positions') }}</span>
            <ArrowTopRightOnSquareIcon class="ml-3 h-5 w-5 flex-shrink-0 text-gray-400" aria-hidden="true" />
          </NuxtLink>
        </div>
      </div> -->


</template>

<script setup>
import { ArrowTopRightOnSquareIcon, EnvelopeIcon, PhoneIcon, XMarkIcon } from '@heroicons/vue/24/outline'
// import kwesforms from 'kwesforms';

//   import { onMounted } from 'vue'; 

//   onMounted(() => {
//      kwesforms.init(); 
//   })

const { locale } = useI18n();

const lang = locale.value;


const offices = [


  { id: 1, city: 'Location', address: ['Langestraat 89/B4', 'Oostende 8400'] },
  { id: 2, city: 'Contact', address: ['info@A-OS.com', ''] },
  { id: 3, city: 'VAT Number', address: ['BE 0784610234', 'KBC 37.983.155'] },
  { id: 4, city: 'IBAN', address: ['BE 22 7310 5403 6247', 'KBC: KREDBEBB'] },
]


const { t } = useI18n({ useScope: "local" });
</script>

<i18n lang="json">
{  
"da": {
"title": "Lad os arbejde sammen",
"subtitle": "Vi vil gerne høre fra dig! Send os en besked ved hjælp af formularen nedenfor eller send en e-mail.",
"contactfirstname":"Fornavn",
"contactlastname":"Efternavn",
"contactcompany":"Virksomhed",
"contactemail":"E-mail",
"contacttel":"Telefonnr.",
"contactmessage":"Besked",
"contactsend":"Send besked",
"office":"Vores kontor",
"location":"Placering",
"contact":"Kontakt",
"vat":"CVR-nummer",
"payment":"IBAN",
"hiretitle":"På udkig efter en ny karriere?",
"hiresubtitle":"Vi ansætter.",
"positions":"Se ledige stillinger"
},
"de": {
"title": "Lass uns zusammenarbeiten",
"subtitle": "Wir würden gerne von Ihnen hören! Senden Sie uns eine Nachricht über das Formular unten oder per E-Mail.",
"contactfirstname":"Vorname",
"contactlastname":"Nachname",
"contactcompany":"Firma",
"contactemail":"E-Mail",
"contacttel":"Telefonnummer",
"contactmessage":"Nachricht",
"contactsend":"Nachricht senden",
"office":"Unser Büro",
"location":"Standort",
"contact":"Kontakt",
"vat":"USt-IdNr.",
"payment":"IBAN",
"hiretitle":"Auf der Suche nach einer neuen Karriere?",
"hiresubtitle":"Wir stellen ein.",
"positions":"Offene Stellen anzeigen"
},
  "en": {
    "title": "Let's work together",
    "subtitle": "We’d love to hear from you! Send us a message using the form opposite, or email us.",
    "contactfirstname":"First Name",
    "contactlastname":"Last Name",
    "contactcompany":"Company",
    "contactemail":"Email",
    "contacttel":"Phone Nr.",
    "contactmessage":"Message",
    "contactsend":"Send Message",
    "office":"Our office",
    "location":"Location",
    "contact":"Contact",
    "vat":"VAT Number",
    "payment":"IBAN",
    "hiretitle":"Looking for a new career?",
    "hiresubtitle":"We’re hiring.",
    "positions":"See open positions",
    },
"es": {
"title": "Trabajemos juntos",
"subtitle": "¡Nos encantaría saber de ti! Envíanos un mensaje utilizando el formulario de al lado o envíanos un correo electrónico.",
"contactfirstname":"Nombre",
"contactlastname":"Apellido",
"contactcompany":"Empresa",
"contactemail":"Correo electrónico",
"contacttel":"Teléfono",
"contactmessage":"Mensaje",
"contactsend":"Enviar mensaje",
"office":"Nuestra oficina",
"location":"Ubicación",
"contact":"Contacto",
"vat":"Número de IVA",
"payment":"IBAN",
"hiretitle":"¿Buscas una nueva carrera?",
"hiresubtitle":"Estamos contratando.",
"positions":"Ver puestos vacantes"
},
"fr": {
"title": "Travaillons ensemble",
"subtitle": "Nous serions ravis de vous entendre ! Envoyez-nous un message en utilisant le formulaire ci-contre, ou envoyez-nous un e-mail.",
"contactfirstname":"Prénom",
"contactlastname":"Nom de famille",
"contactcompany":"Société",
"contactemail":"E-mail",
"contacttel":"Numéro de téléphone",
"contactmessage":"Message",
"contactsend":"Envoyer le message",
"office":"Notre bureau",
"location":"Emplacement",
"contact":"Contact",
"vat":"Numéro de TVA",
"payment":"IBAN",
"hiretitle":"À la recherche d'une nouvelle carrière ?",
"hiresubtitle":"Nous recrutons.",
"positions":"Voir les postes ouverts"
},
"nl": {
"title": "Laten we samenwerken",
"subtitle": "We horen graag van u! Stuur ons een bericht via het formulier hiernaast of stuur ons een e-mail.",
"contactfirstname":"Voornaam",
"contactlastname":"Achternaam",
"contactcompany":"Bedrijf",
"contactemail":"E-mail",
"contacttel":"Telefoonnummer",
"contactmessage":"Bericht",
"contactsend":"Bericht verzenden",
"office":"Ons kantoor",
"location":"Locatie",
"contact":"Contact",
"vat":"BTW-nummer",
"payment":"IBAN",
"hiretitle":"Op zoek naar een nieuwe carrière?",
"hiresubtitle":"We zijn aan het werven.",
"positions":"Bekijk open posities"
}
}
</i18n>
    


     


