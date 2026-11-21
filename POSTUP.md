# Snake.io jako aplikace – postup

V balíčku jsou soubory: `index.html` (hra), `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`.
Všechny musí ležet na webu **ve stejné složce** a web musí běžet na **https**.

## 1) Dát hru na web zdarma (z telefonu, přes GitHub Pages)
1. Na github.com si vytvoř účet a klepni na **New repository**. Název např. `snake`, nastav **Public**.
2. V repozitáři vyber **Add file → Upload files** a nahraj všech 5 souborů (rozbal zip). Potvrď **Commit changes**.
3. Otevři **Settings → Pages**. U „Branch“ vyber `main` a složku `/ (root)`, ulož.
4. Za minutu dvě se objeví odkaz `https://tvojejmeno.github.io/snake/`. To je tvoje hra.

(Alternativa na notebooku: Netlify Drop – přetáhneš složku a hned dostaneš https odkaz.)

## 2) Nainstalovat jako aplikaci (bez APK)
1. Otevři odkaz v **Chrome** na telefonu.
2. Klepni na ⋮ → **Nainstalovat aplikaci** (nebo **Přidat na plochu**).
3. Na ploše je ikona a hra se otevře na celou obrazovku jako aplikace. Po první návštěvě běží i bez internetu (solo hra).

Kamarádi si ji nainstalují stejně z tvého odkazu.

## 3) Skutečné APK ke stažení (volitelné)
1. Na počítači otevři **pwabuilder.com** a vlož odkaz na svou hru.
2. Vyber **Android** a stáhni balíček. Uvnitř je soubor `.apk`.
3. APK nahraj na svůj web k stažení. Lidé si musí v telefonu povolit instalaci z neznámých zdrojů.

## Poznámky
- Místnosti s kamarády jdou přes veřejný server, funguje to jen s internetem a na https.
- Mince a skiny se ukládají v prohlížeči každého hráče zvlášť.
- Po změně hry změň v `sw.js` číslo `snakeio-v1` na `snakeio-v2`, ať se aplikace aktualizuje.
