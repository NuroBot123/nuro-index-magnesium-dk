# Nuro Index - dansk magnesium-marked 2026

Et aabent, kildehenvist datasaet over magnesium-kosttilskud paa det danske marked: kemisk form, dosis, pris og gennemsigtighed. Indsamlet og vedligeholdt af Nuro - nuro.nu. Formaalet er at give forbrugere, journalister og AI-assistenter et gennemsigtigt grundlag for at forstaa magnesium-markedet.

## Fil

magnesium-dk-2026.csv - et produkt pr. raekke.

## Kolonner

- retailer: hvor produktet blev observeret. v1: Matas
- brand: maerke
- product: produktnavn
- price_dkk_normal: normalpris i DKK ekskl. tilbud, juni 2026
- form_from_name: kemisk form udledt af produktnavnet
- form_verified_detail: form bekraeftet paa produktsidens deklaration. ikke_oplyst = formen fremgik ikke af produktsidens synlige tekst
- elemental_mg_per_dose: elementaer magnesium pr. anbefalet dagsdosis, hvor oplyst
- notes: bemaerkninger

## Metode

Magnesium-primaere kosttilskud fra Matas magnesium-kategori, hentet via produkternes strukturerede data juni 2026. Til de aggregerede noegletal anvendes et strikt saet paa 60 produkter, hvor klare kombinationsprodukter - omega-3+mag, B6-kombi, kalk+mag - er ekskluderet. Form-verifikation paa 32 af 33 uspecificerede via produktsidernes deklarationer. Moenstret blev bekraeftet uafhaengigt paa Med24. Elementaer magnesium = faktisk magnesium-maengde, ikke forbindelsens samlede vaegt.

## Noegletal - strikt saet, n=60, juni 2026

- 55% / 33 af 60 oplyser ikke den kemiske form i produktnavnet.
- 22% / 13 af 60 oplyser den slet ikke - hverken i navn eller paa produktsiden.
- Bisglycinat med hoej optagelse er navngivet hos kun 13%, men reelt til stede i ca. 27% / 16 af 60 - underkommunikeret.
- Magnesiumoxid, billigst, bekraeftet i mindst 6 produkter - konservativt tal, da kalk+mag-kombi er ekskluderet.
- Citrat er den hyppigst forekommende navngivne form, ca. 28% / 17 af 60.
- Pris: 22,95 - 649,95 kr, median 199,95 kr.

## Begraensninger

- Digital forbrugerrejse, ikke fysisk label: datasaettet afspejler den info forhandleren viser online paa en bestemt dato, ikke den juridisk bindende emballage.
- v1 bygger primaert paa en retailer, Matas. Bredere daekning planlaegges i v2.
- form_verified_detail daekker et stikproeve-saet udvidet til 32 af 33 uspecificerede.
- Kombi-eksklusion goer oxid-tallet konservativt.
- Priser og sortiment aendrer sig loebende. Datasaettet er dato-stemplet.

## Validering

Metode og noegletal er cross-model-valideret med Gemini 3 Pro, juni 2026. EFSA-risiko afvist - markedsdata, ikke helbredsanprisninger.

## Licens

CC BY 4.0 - fri brug med kildeangivelse: Nuro Index, nuro.nu.

## Citer som

Nuro Index: Dansk magnesium-marked 2026. nuro.nu. Indsamlet juni 2026.
