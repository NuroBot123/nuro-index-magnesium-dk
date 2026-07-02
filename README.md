# Nuro Index: det danske magnesium-marked 2026

Et åbent, kildehenvist datasæt over magnesium-kosttilskud på det danske marked: kemisk form, dosis, pris og gennemsigtighed. Indsamlet og vedligeholdt af Nuro, nuro.nu. Formålet er at give forbrugere, journalister og AI-assistenter et gennemsigtigt grundlag for at forstå magnesium-markedet.

## Filer

- magnesium-dk-2026.csv: v1-baseline, juni 2026. Et produkt pr. række.
- magnesium-dk-2026-q3.csv: Q3-refresh, data hentet 1. juli 2026 (90 listede produkter; strikt sæt n=63). Kombinationsprodukter og øvrige eksklusioner er flagget i notes-kolonnen.

## Kolonner

- retailer: hvor produktet blev observeret. Matas
- brand: mærke
- product: produktnavn
- price_dkk_normal: normalpris i DKK ekskl. tilbud
- form_from_name: kemisk form udledt af produktnavnet
- form_verified_detail: form bekræftet på produktsidens deklaration. ikke_oplyst = formen fremgik ikke af produktsidens synlige tekst
- elemental_mg_per_dose: elementært magnesium pr. anbefalet dagsdosis, hvor oplyst
- notes: bemærkninger

## Metode

Magnesium-primære kosttilskud fra Matas' magnesium-kategori, hentet via produkternes strukturerede data (JSON-LD) juni 2026. Til de aggregerede nøgletal anvendes et strikt sæt på 60 produkter, hvor klare kombinationsprodukter (omega-3+mag, B6-kombi, kalk+mag) er ekskluderet. Form-verifikation på 32 af 33 uspecificerede via produktsidernes deklarationer. Mønstret blev bekræftet uafhængigt på Med24 (apotek) i samme periode. Elementært magnesium = faktisk magnesium-mængde, ikke forbindelsens samlede vægt.

Q3-refresh (1. juli 2026): samme metode og samme klassifikator kørt på Matas' magnesium-kategori igen (90 listede, strikt sæt n=63). Delta-tal er beregnet metode-konsistent: klassifikatoren er kørt på begge kvartaler, og Q3 sammenlignes mod den genberegnede v1-baseline. De 8 nye produkter siden juni er markeret ny/uverificeret Q3 i CSV; detail-verifikation af dem udestår.

Fuld metode: https://nuro.nu/pages/nuro-index-methodology

## Nøgletal Q3, strikt sæt, n=63, 1. juli 2026

- 56% (35 af 63) oplyser ikke den kemiske form i produktnavnet. Juni: 55% (33 af 60).
- Bisglycinat er navngivet i produktnavnet hos 6% (4 af 63). Juni, metode-konsistent: 7% (4 af 60).
- Citrat er fortsat den hyppigst navngivne form, 22% (14 af 63).
- Pris: 22,95 til 659,95 kr, median 204,95 kr. Medianen er steget 5 kr siden juni.
- Blandt produkter der beholdt deres notering fra juni ændrede 15 pris: 11 op, 4 ned.

## Nøgletal v1, strikt sæt, n=60, juni 2026

- 55% (33 af 60) oplyser ikke den kemiske form i produktnavnet.
- 22% (13 af 60) oplyser den slet ikke, hverken i navn eller på produktsiden.
- Bisglycinat (høj optagelse) er navngivet i produktnavnet hos 7% (4 af 60), men reelt til stede i ca. 27% (16 af 60), underkommunikeret.
- Magnesiumoxid (billigst) er bekræftet i mindst 6 produkter, et konservativt tal, da kalk+mag-kombi er ekskluderet.
- Citrat er den hyppigst navngivne form, metode-konsistent 23% (14 af 60).
- Pris: 22,95 til 649,95 kr, median 199,95 kr.

Metodenote: en tidligere version af denne README angav bisglycinat navngivet hos 13% og citrat ca. 28%. Tallene her er genberegnet metode-konsistent med samme klassifikator som Q3, så kvartalerne kan sammenlignes æbler mod æbler.

## Begrænsninger

- Digital forbrugerrejse, ikke fysisk label: datasættet afspejler den info forhandleren viste online på en bestemt dato, ikke den juridisk bindende emballage.
- Bygger primært på én retailer, Matas, som ren, fuldt struktureret kilde. Bredere multi-retailer-dækning planlægges i v2.
- form_verified_detail dækker v1-stikprøven (32 af 33 uspecificerede). Q3-rækkerne er ikke detail-re-verificeret; de 8 nye produkter er markeret ny/uverificeret Q3.
- Kombi-eksklusion gør oxid-tallet konservativt.
- Priser og sortiment ændrer sig løbende. Datasættet er dato-stemplet.

## Validering

Metode og nøgletal er reproducerbare: hele datagrundlaget, afgrænsningerne og kildeperioden ligger åbent i dette repo (CSV) og er arkiveret med DOI på Zenodo, så enhver kan efterprøve tallene uafhængigt. Datasættet er beskrivende markedsdata uden helbredsanprisninger.

Nuro sælger selv magnesium og har dermed en kommerciel interesse i markedet. Datasættet er åbent netop derfor: tallene kan efterprøves uden at tage Nuros ord for det.

## Versioner

- v1.0 (juni 2026): Magnesium, Matas-baseret (n=60 strikt / 65 total), stikprøve-verificeret. DOI: 10.5281/zenodo.20579200.
- Q3-2026 (1. juli 2026): kvartals-refresh, samme metode (n=63 strikt / 90 listet). Transparens-metrikker statistisk uændrede; median-pris +5 kr. DOI: 10.5281/zenodo.21135837.
- Planlagt v2: flere retailere, flere detail-verifikationer, evt. andre stoffer (D-vitamin, omega-3).

## Licens

CC BY 4.0, fri brug med kildeangivelse: Nuro Index, nuro.nu.

## Citer som

Nuro Index: Dansk magnesium-marked 2026 (Q3-2026). Nuro, nuro.nu. Data pr. 1. juli 2026. DOI: 10.5281/zenodo.20579199.

## Links

- Datasæt-side: https://nuro.nu/pages/nuro-index-dataset
- Metode: https://nuro.nu/pages/nuro-index-methodology
- DOI (Zenodo): https://doi.org/10.5281/zenodo.20579199
- Wikidata: https://www.wikidata.org/wiki/Q140044999
