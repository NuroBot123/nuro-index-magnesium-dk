# Nuro Index: det danske magnesium-marked 2026

Et åbent, kildehenvist datasæt over magnesium-kosttilskud på det danske marked: kemisk form, dosis, pris og gennemsigtighed. Indsamlet og vedligeholdt af Nuro, nuro.nu. Formålet er at give forbrugere, journalister og AI-assistenter et gennemsigtigt grundlag for at forstå magnesium-markedet.

## Fil

magnesium-dk-2026.csv, et produkt pr. række.

## Kolonner

- retailer: hvor produktet blev observeret. v1: Matas
- brand: mærke
- product: produktnavn
- price_dkk_normal: normalpris i DKK ekskl. tilbud, juni 2026
- form_from_name: kemisk form udledt af produktnavnet
- form_verified_detail: form bekræftet på produktsidens deklaration. ikke_oplyst = formen fremgik ikke af produktsidens synlige tekst
- elemental_mg_per_dose: elementært magnesium pr. anbefalet dagsdosis, hvor oplyst
- notes: bemærkninger

## Metode

Magnesium-primære kosttilskud fra Matas' magnesium-kategori, hentet via produkternes strukturerede data (JSON-LD) juni 2026. Til de aggregerede nøgletal anvendes et strikt sæt på 60 produkter, hvor klare kombinationsprodukter (omega-3+mag, B6-kombi, kalk+mag) er ekskluderet. Form-verifikation på 32 af 33 uspecificerede via produktsidernes deklarationer. Mønstret blev bekræftet uafhængigt på Med24 (apotek) i samme periode. Elementært magnesium = faktisk magnesium-mængde, ikke forbindelsens samlede vægt.

Fuld metode: https://nuro.nu/pages/nuro-index-methodology

## Nøgletal, strikt sæt, n=60, juni 2026

- 55% (33 af 60) oplyser ikke den kemiske form i produktnavnet.
- 22% (13 af 60) oplyser den slet ikke, hverken i navn eller på produktsiden.
- Bisglycinat (høj optagelse) er navngivet hos kun 13%, men reelt til stede i ca. 27% (16 af 60), underkommunikeret.
- Magnesiumoxid (billigst) er bekræftet i mindst 6 produkter, et konservativt tal, da kalk+mag-kombi er ekskluderet.
- Citrat er den hyppigst navngivne form, ca. 28% (17 af 60).
- Pris: 22,95 til 649,95 kr, median 199,95 kr.

## Begrænsninger

- Digital forbrugerrejse, ikke fysisk label: datasættet afspejler den info forhandleren viste online på en bestemt dato, ikke den juridisk bindende emballage.
- v1 bygger primært på én retailer, Matas, som ren, fuldt struktureret kilde. Bredere multi-retailer-dækning planlægges i v2.
- form_verified_detail dækker et stikprøve-sæt udvidet til 32 af 33 uspecificerede.
- Kombi-eksklusion gør oxid-tallet konservativt.
- Priser og sortiment ændrer sig løbende. Datasættet er dato-stemplet.

## Validering

Metode og nøgletal er reproducerbare: hele datagrundlaget, afgrænsningerne og kildeperioden ligger åbent i dette repo (CSV) og er arkiveret med DOI på Zenodo, så enhver kan efterprøve tallene uafhængigt. Datasættet er beskrivende markedsdata uden helbredsanprisninger.

Nuro sælger selv magnesium og har dermed en kommerciel interesse i markedet. Datasættet er åbent netop derfor: tallene kan efterprøves uden at tage Nuros ord for det.

## Versioner

- v1.0 (juni 2026): Magnesium, Matas-baseret (n=60 strikt / 65 total), stikprøve-verificeret. DOI: 10.5281/zenodo.20579200.
- Planlagt v2: flere retailere, flere detail-verifikationer, evt. andre stoffer (D-vitamin, omega-3).

## Licens

CC BY 4.0, fri brug med kildeangivelse: Nuro Index, nuro.nu.

## Citer som

Nuro Index: Dansk magnesium-marked 2026 (v1.0). Nuro, nuro.nu. Indsamlet juni 2026. DOI: 10.5281/zenodo.20579199.

## Links

- Datasæt-side: https://nuro.nu/pages/nuro-index-dataset
- Metode: https://nuro.nu/pages/nuro-index-methodology
- DOI (Zenodo): https://doi.org/10.5281/zenodo.20579199
- Wikidata: https://www.wikidata.org/wiki/Q140044999
