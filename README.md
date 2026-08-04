# Aktsiajälgija – seadistamise juhend

Selle juhendiga saad oma aktsiajälgija veebi üles ja AI-analüüsi tööle. Kõik on tasuta. Aega kulub ~10 minutit.

Rakendus: üks `index.html` fail, mis näitab aktsiate ja ETF-ide hindu (Yahoo Finance), arvutab tehnilise OSTA/HOIA/MÜÜ signaali ja küsib soovi korral Gemini AI-lt analüüsi.

---

## 1. Rakenduse üleslaadimine GitHubi

Vaja on GitHubi kontot (github.com → Sign up, kui pole).

1. Ava **github.com/new**
2. Repository name: pane lühike nimi, nt `akt`
3. Jäta **Public** valituks → **Create repository**
4. Vajuta **uploading an existing file** linki
5. Vali `index.html` fail → **Commit changes**

## 2. GitHub Pages sisselülitamine

See teeb failist päris veebilehe.

1. Ava **github.com/SINU-KASUTAJA/akt/settings/pages**
2. "Build and deployment" → Branch: vali **main**, kaust **/ (root)** → **Save**
3. Oota 1–2 minutit
4. Sinu rakendus töötab aadressil: `https://SINU-KASUTAJA.github.io/akt`

Kui näed 404 – Pages pole veel valmis ehitatud, oota minut ja värskenda.

## 3. Telefoni avakuvale lisamine

1. Ava rakenduse aadress telefonis Chrome'is
2. Menüü (⋮) → **Lisa avakuvale** → Lisa

Rakendus avaneb nüüd täisekraanil nagu tavaline äpp.

## 4. Gemini API võtme loomine (AI-analüüsi jaoks, valikuline)

Võti on tasuta. Vaja on Google'i kontot.

1. Ava **aistudio.google.com/apikey** ja logi sisse
2. Vajuta **Create API key**
3. Kopeeri võti (koopia ikoon võtme kõrval)
4. Ava oma rakendus → **⚙ AI-analüüsi seaded** → kleebi võti Gemini välja

**Ära vajuta "Set up billing"** – tasuta tase töötab ilma ja nii ei saa kogemata arvet tekkida.

Võti salvestub ainult sinu seadmesse. Ära jaga seda kellegagi ega pane koodi sisse.

## 5. Kasutamine

- **Lisa instrument**: sisesta sümbol (nt `AAPL`, `TSLA`; Frankfurdi Xetra ETF-id lõpuga `.DE`, nt `SXR8.DE`) → + Lisa
- **Detailid**: vajuta instrumendi real – avaneb soovitus, põhjendus, analüüsilingid
- **AI-analüüs**: detailvaates "Küsi AI analüüsi" (vajab Gemini võtit)
- **Eemaldamine**: detailvaate all "× Eemalda jälgimisest"
- **Graafiku vahemik**: Päev / Kuu / Aasta / Kogu aeg

## Tasuta limiidid

- Gemini tasuta tase: piisab mitmekümneks analüüsiks päevas. Rakendus hoiab limiiti kokku: sama analüüsi ei küsita 30 min jooksul uuesti.
- Kui tuleb teade "limiit täis" – oota minut ja proovi uuesti.

## Kui midagi ei tööta

- **404 rakenduse aadressil** → Pages pole sisse lülitatud (samm 2)
- **Vana versioon näha** → tõmba leht sõrmega alla värskendamiseks või ava inkognito aknas
- **"ei saanud andmeid"** → vajuta ↻ uuesti; kontrolli, et sümbol on õige
- **Gemini viga** → kontrolli, et võti on täies pikkuses kopeeritud

---

*NB! Rakenduse soovitused on lihtsustatud tehnilised indikaatorid, mitte investeerimisnõustamine. Otsused tee ise.*
