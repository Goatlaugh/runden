# Runden

Første kopi av Familiemajoren versjon 1.60.

## Hva som er gjort (første steg)

- Eget navn: **Runden**
- Adskilte data: alle localStorage-nøkler er endret fra `familiemajoren_*` til `runden_*`
- Eget service worker-cache: `runden-v1`
- Eget manifest med egen `id` og `start_url`
- Sky-nøkler er tomme (egen Supabase må settes opp)
- Charteret er fortsatt med (fjernes i neste steg)
- Utseende, farger, bilder og logo er **uendret** (samme filer som originalen)
- Baneboken bruker samme filformat (eksport/import begge veier fungerer)

## Bekreftelse

Når denne appen legges til på hjemskjermen på samme telefon som Familiemajoren:
- Data blandes ikke (forskjellige localStorage-nøkler)
- Cache blandes ikke (forskjellig SW-navn)
- Familiemajoren forblir urørt

## Neste steg (etter bekreftelse)

1. Egen logo, bilder og farger
2. Fjerne charteret helt
3. Tilpasse tekster for vanlige runder, private helger, éndags-arrangement og den årlige golfturen
4. Sette opp egen Supabase-prosjekt og fylle inn `CLOUD_URL` og `CLOUD_KEY` i `index.html`

## Filer

- `index.html` – hele appen
- `sw.js` – service worker
- `manifest.webmanifest` – PWA-manifest
- `cast.html` – for Chromecast
- Bilder og ikoner må kopieres fra originalen (banner.jpg, icon-*.png, osv.) for at utseendet skal være identisk

## Hvordan teste

1. Kopier alle filer (inkludert bilder fra originalen) til en webserver eller GitHub Pages i egen mappe
2. Åpne på telefon
3. Legg til på hjemskjermen
4. Verifiser at Familiemajoren fortsatt fungerer uendret
