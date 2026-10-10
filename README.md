# Kast – installeren op je iPhone

Kast is een web-app: één keer online zetten, daarna opent hij vanaf je beginscherm als een gewone app. Je kleding en foto's blijven op je iPhone staan; alleen het weer wordt opgehaald (bij Open-Meteo, gratis en zonder account).

## 1. Online zetten met GitHub Pages (± 5 minuten, gratis)

1. Maak een account op github.com (als je er nog geen hebt).
2. Klik rechtsboven op **+ → New repository**. Naam: `kast`. Zet hem op **Public** en klik **Create repository**.
3. Klik op **uploading an existing file** en sleep alle bestanden uit deze map erin:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`.
   Klik **Commit changes**.
4. Ga naar **Settings → Pages**. Bij *Source* kies je **Deploy from a branch**, branch **main**, map **/ (root)**, en klik **Save**.
5. Na een minuutje staat je app op `https://<jouw-gebruikersnaam>.github.io/kast/`.

> Tip: de repository is publiek, maar daar staat alleen de code. Je kleding, foto's en draaggeschiedenis staan nooit online.

## 2. Op je beginscherm zetten

1. Open de link in **Safari** op je iPhone.
2. Tik op het **deelicoon** → **Zet op beginscherm** → **Voeg toe**.
3. Open Kast voortaan via het icoon. Gebruik altijd dat icoon: de app op je beginscherm heeft zijn eigen opslag, los van Safari.

## 3. Eerste keer

1. **Vandaag → Gebruik mijn locatie** (of zoek je stad in Instellingen).
2. **Kast → Toevoegen**: fotografeer elk stuk tegen een effen achtergrond, kies soort, kleur, warmte en gelegenheden.
   Met *Opslaan en nog een toevoegen* gaat dat snel achter elkaar.
3. Stel bij **Aantal keer dragen tot de was** in hoe vaak iets mee mag: standaard 1× voor tops, 3× voor truien, 4× voor broeken, en "Nooit" voor jassen en schoenen.

## Automatisch herkennen instellen

Kast kan bij elke foto zelf bepalen wat het is (t-shirt, trui, jas, broek…), welke kleur, hoe warm (dunne of dikke trui) en voor welke gelegenheden. Dat gebeurt via Claude, met je eigen API-sleutel.

1. Ga op je computer naar **console.anthropic.com** en maak een account. Dit staat los van een Claude.ai-abonnement.
2. Zet een klein tegoed op je account (bij **Billing**) en stel een **maandlimiet** in, zodat je nooit verrast wordt.
3. Ga naar **API Keys → Create Key** en kopieer de sleutel (begint met `sk-ant-`).
4. In Kast: **Instellingen → Automatisch herkennen**, plak de sleutel en tik **Bewaar**.

Daarna vult Kast na elke foto alles zelf in; jij controleert alleen. In **Kast** verschijnt ook **Meerdere foto's toevoegen**: kies in één keer een hele reeks foto's uit je bibliotheek. Automatisch toegevoegde stukken krijgen een geel label *nakijken* tot je ze één keer opent en opslaat.

De sleutel blijft op je iPhone, gaat alleen naar Anthropic en zit niet in je back-ups.

## Dagelijks gebruik

- 's Ochtends open je Kast: je ziet het weer en een outfit voor de gelegenheid (weekdag = Werk, weekend = Casual; aanpasbaar).
- **Andere outfit** voor een alternatief, of tik op één stuk om alleen dat te wisselen.
- **Ik draag dit** telt een draagbeurt. Is het maximum bereikt, dan gaat het naar de **Wasmand** en wordt het niet meer voorgesteld.
- Na het wassen: **Wasmand → Gewassen** (per stuk of alles tegelijk).
- Iets twee dagen na elkaar dragen wordt sowieso vermeden, ook als het nog niet in de was moet.

## Automatisch elke ochtend openen (optioneel)

iPhone-app **Opdrachten** → **Automatisering** → **+** → **Tijdstip** (bv. 7:00, weekdagen) → **Voer direct uit** → actie **Open app** → kies **Kast**.

## Back-up

Instellingen → **Back-up maken** en bewaar het bestand in iCloud Drive. Verwijder je de app van je beginscherm, dan is je kast weg, tenzij je een back-up hebt.

## Updates

Pas je later iets aan, upload dan de nieuwe `index.html` naar dezelfde repository. Verhoog ook het versienummer (`kast-v2` → `kast-v3`) in `sw.js`, zodat je iPhone de nieuwe versie ophaalt.
