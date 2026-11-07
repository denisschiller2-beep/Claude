# Kompletní předání projektu Kurfürst CO. (pro lokální Claude Code na Macu)

Stav k 7. 11. 2026. Tento soubor shrnuje vše, co jsme zatím probrali, udělali a co zbývá.
Repozitář: `denisschiller2-beep/Claude`, větev `claude/wix-website-management-etu8bc`
(obsahuje i `CLAUDE.md`, zálohy a návrhy textů).

---

## 1. Jak se mnou pracovat

- Piš **česky, stručně, jen důležité info**. „Proč“ vysvětli jednou větou, jen když je potřeba.
- **Nic nepublikuj na živý web bez mého souhlasu.** Úpravy v editoru ukládej jako koncept,
  publikuju až já po kontrole náhledu. Hromadné e-maily (newsletter) odesílám vždy já.
- U změn vzhledu nejdřív **návrh** (barvy, fonty, struktura), realizace až po schválení.
- **Kontroluj fakta** v mých textech a dej vědět, když jde něco opravit nebo udělat líp.
- Vždy hledej řešení. Když něco nejde, navrhni jinou cestu, a to tu **nejefektivnější**.
- Data (produkty, texty, SEO, kategorie, blog) měň přes **Wix API (konektor Wix)**.
  Vzhled, rozložení a mobil měň v **editoru přes Claude in Chrome**.
- Po každém větším kroku aktualizuj `CLAUDE.md` (stav + deník rozhodnutí) a commitni ho.

---

## 2. Firma a web

| Údaj | Hodnota |
|---|---|
| Firma | **Kurfürst CO., s.r.o.**, minerály, drahé kameny, ručně pletené náramky, srdce z kamenů |
| Wix web | **KURFÜRST CO., s.r.o.**, Site ID `4e547b0e-3546-40c0-9085-36e85fccbe29` |
| URL | https://denisschiller2.wixsite.com/kurf-rst-co---s-r-o (zveřejněný, zatím bez vlastní domény) |
| Plán | **Free**, záměrně. Předplatné koupím až před spuštěním prodeje. |
| Editor | klasický Wix Editor, Velo zapnuté |
| Obchod | Wix Stores, **Catalog V3** (používat jen `/stores/v3/` endpointy), 235 produktů, 24 kategorií |
| Jazyk / měna | čeština, CZK, Europe/Prague; nainstalovaný Wix Multilingual |
| Aplikace | Instagram Feed, Promote SEO, Wix Chat, Forms & Payments, Hotels, Invoices (V1), Pay Links |
| Blog | **není nainstalovaný** |
| Kontakt na webu | kurfurst.pv@volny.cz |

V účtu jsou ještě 2 staré nezveřejněné koncepty z 2/2023 („Kurfürst CO., s.r.o.“ s ID `57ea19a9-…`
a „My Site 1“). **Nesahat na ně.**

**Předplatné:** podle Wix Help Center jde obchod nastavit zdarma, ale **přijímat platby lze až od
plánu Core výš** (Light platby neumí).

---

## 3. Hlavní rozhodnutí

- **Varianta A (schváleno):** do Vánoc rychlá prodejní verze (oprava produktů, SEO, mobil,
  začátkem prosince předplatné a spuštění prodeje). Velký redesign dotáhneme přes zimu.
- **Reklamy až po spuštění plateb**, jinak se platí za návštěvy, které nemohou nakoupit.
- **Popisy produktů krátké** (1–2 věty + údaje). **Dlouhé texty o minerálech** patří do
  **popisu kategorie** (dnes jsou schované v jednom produktu na začátku kategorie a kategorie
  popis nemají).
- **Léčivé účinky** (astma, imunita, trávení, migrény…) z textů **odstranit**. Ponechat jen
  tradiční a duchovní význam („bývá spojován s…“).
- Na fotce je vždy **přesně ten kus**, který zákazník dostane. Do popisů napsat
  „Na fotce je přesně tento kus, každý kámen je originál.“
- URL adresy (slugy) produktů **neměnit**, aby nevznikly nefunkční odkazy.

---

## 4. Co je hotové

1. **Audit produktů:** všech 235 je viditelných a má fotku i kategorii, 14 je vyprodaných.
   Původně mělo 193 produktů stejný název jako jiné (27× „Prasopál“ apod.).
2. **Přejmenováno 174 kamenů** (bulk update přes API, 0 chyb) na formát
   `Minerál – Lokalita · největší rozměr cm, hmotnost`, např.
   „Fluorit – Loralai, Pákistán · 28 cm, 4,65 kg“. Lokality jsem sjednotil česky.
   Záloha původních názvů: `zalohy/2026-11-04-puvodni-nazvy-produktu.json`.
3. **Přejmenováno 15 náramků:** do názvu přibyla barva provázku odečtená z fotek, např.
   „Ručně pletený náramek s růženínem – vínový provázek“.
4. **Kontrola faktů** ve všech dlouhých textech a **návrh nových textů**:
   `texty/navrh-textu-2026-11-04.md`. Obsahuje tabulku chyb, opravené texty kategorií,
   nové texty pro minerály bez popisu a šablony krátkých popisů produktů.
   **Zatím nic z toho není na webu.**
5. Paměť projektu `CLAUDE.md` a tento soubor jsou na GitHubu.

### Nejdůležitější nalezené chyby v mých textech (detail v souboru textů)
- Rubín v zoisitu: hlavní lokalita je Longido / důl **Mundarara**, ne Merelani (tam je tanzanit).
  Černá zrna jsou amfibol, ne zoisit.
- Prasopál: je to zelený **opál** (nikl), tvrdost 5,5–6,5, ne odrůda chalcedonu.
- Ametyst: věta o vodních filtrech, polovodičích a senzorech je nepravdivá.
- Labradorit: misionáři Moravské církve, ne „čeští“; Slovensko vyřazeno, přidáno Finsko.
- Apofylit není zeolit (jen stilbit). Pentagonit není zeolit a název má podle pětiúhelníkového
  průřezu krystalů.
- Purpurit: Kalahari Manganese Field je v JAR, ne v Namibii.
- Sluneční kámen: třpyt dělá většinou hematit, ne měď.
- Smaragd z Afghánistánu: v textu chybí Afghánistán (Pandžšír).
- Amazonit: „schiller efekt“ není typický; kombinace se záhnědou je z Colorada, ne z Brazílie.

---

## 5. Co čeká na moje potvrzení

- [ ] **Schválit texty** v `texty/navrh-textu-2026-11-04.md`. Pak je zapsat:
      dlouhé texty do popisů kategorií, krátké popisy ke všem produktům.
- [ ] **3× Prasopál** se stejnými údaji 9 cm / 111 g (`prasopál-13`, `prasopál-3`, `prasopál-1`):
      jsou to různé kameny, nebo omylem zdvojený produkt?
- [ ] **Doplnit chybějící údaje:** `prasopál-35` (950 Kč) nemá rozměry ani hmotnost,
      `tanzanit-1` nemá hmotnost.
- [ ] **Akvamaríny „Balúčistán, Pákistán“:** ověřit u dodavatele. Pákistánské akvamaríny jsou
      typicky ze severu (Gilgit-Baltistán).
- [ ] Barvy provázků: jeden fluoritový náramek je „purpurový“, druhý „fialový“. Sedí to?

---

## 6. Co dál udělat (pořadí podle varianty A)

### Přes API
1. Po schválení zapsat **texty kategorií** a **krátké popisy produktů** (opravit i překlep
   v `akvapras-zimbabwe-8`, kde je v popisu „Lokalita: Akvapras“ místo Zimbabwe).
2. **Sjednotit názvy zbylých ~42 produktů** do stejného formátu. Nekonzistence:
   „Fuorit“ (překlep), „Akvapras- Zimbabwe“, „Akvapras -Zimbabwe“, „Modrý Chalcedon“,
   „Růženín -leštěný“, „Spinel - Tanzánie“, „Fluorit - Kongo“ apod. Zbylé 4 náramky
   (sluneční kámen, rubín v zoisitu, čaroit, karneol) doplnit o barvu provázku.
3. Kategorie: prázdné „Titanit/Sphene“ a „Spessartin“ (smazat nebo naplnit), sjednotit
   „Apofylit a Stilbit“.
4. **SEO:** titulky a meta popisy produktů a kategorií, alt texty fotek.
5. **Blog:** nainstalovat Wix Blog, témata navázaná na prodávané kameny (např. „kámen podle
   znamení“, „kámen podle měsíce narození“, dárkový průvodce na Vánoce), články s odkazy
   na produkty.

### V editoru (Claude in Chrome)
6. **Audit** všech stránek na počítači i v **mobilu** a seznam problémů.
7. Ověřit, jestli se **popis kategorie** zobrazuje na stránce kategorie. Když ne, zjistit jak ho
   tam dostat (kvůli SEO).
8. **Rychlé mobilní úpravy** pro Vánoce a návrh nového vzhledu (2 varianty) ke schválení.

### Spuštění (začátek prosince)
9. Předplatné (min. **Core**), vlastní doména, platby, doprava, obchodní podmínky.

### Marketing (až po spuštění plateb)
10. Google Search Console a Merchant Center, profil firmy na Googlu,
    **Heureka a Zboží.cz**, Instagram, reklamy, newsletter.

### Nové minerály
11. Mám na skladě nové minerály. Nafotím je, Claude napíše popisy, zařadí je a nahraje
    (formát názvu a popisu podle bodu 4).

---

## 7. Technické poznámky

- Produkty V3: čtení `POST https://www.wixapis.com/stores/v3/products/query`
  (`fields: ["PLAIN_DESCRIPTION", ...]`, `cursorPaging`), hromadná úprava
  `POST https://www.wixapis.com/stores/v3/bulk/products/update`
  (`products: [{ product: { id, revision, name } }]`, max. 100 na dávku, nutná aktuální `revision`).
  Název produktu má max. 80 znaků.
- Kategorie: `POST https://www.wixapis.com/categories/v1/categories/query` s
  `treeReference: { appNamespace: "@wix/stores", treeKey: null }`.
- Popisy kamenů mají strukturu `Lokalita: … Rozměry (cm - š-v-h): … Hmotnost (g): …`, takže
  se z nich dají údaje vyčíst automaticky.
- Fotky produktů jsou na `static.wixstatic.com`. V cloudu je k tomu osobní prostředí „Claude“,
  lokálně to není potřeba.
