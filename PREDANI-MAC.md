# Předání projektu Kurfürst CO. pro lokální Claude Code na Macu

Stav k 7. 11. 2026. Tento soubor obsahuje vše, co jsme zatím probrali, udělali a co zbývá.
Spolu s ním si přečti `CLAUDE.md` (paměť projektu, načte se automaticky).

Repozitář: `denisschiller2-beep/Claude`, větev `claude/wix-website-management-etu8bc`.

---

## 1. Jak se mnou pracovat

- Piš **česky, stručně, jen důležité info**. „Proč“ vysvětli jednou větou, jen když je potřeba.
- **Nic nepublikuj na živý web bez mého souhlasu.** V editoru ukládej jako koncept. Publikuju až já
  po kontrole náhledu. Hromadné e-maily (newsletter) odesílám vždy já.
- U změn vzhledu nejdřív **návrh** (barvy, fonty, struktura), realizace až po schválení.
- **Kontroluj fakta** a dej vědět, když jde něco opravit nebo udělat líp.
- Vždy hledej **nejefektivnější** řešení. Když něco nejde, navrhni jinou cestu.
- Data (produkty, texty, SEO, kategorie, blog) měň přes **Wix API (konektor Wix)**.
  Vzhled, rozložení a mobil měň v **editoru přes Claude in Chrome**.
- **Před každou hromadnou změnou dat udělej zálohu** do složky `zalohy/`.
- Po každém větším kroku aktualizuj `CLAUDE.md` a změny commitni a pushni.

### Pravidla pro texty
- Přirozená čeština, ne jako překlad. Odborně, ale prodejně, se zajímavostí.
- **Žádné léčivé účinky.** Duchovní význam jen ve tvaru „V esoterice je … spojován s …“.
- Jen ověřená fakta. Když si nejsi jistý, raději vynech.
- **Neuváděj počty kusů ani aktuální sklad** (např. „jeden kus máme z…“). Po prodeji by to mátlo.
  Lokality piš obecně, přesná lokalita je vždy u produktu.

---

## 2. Firma a web

- **Firma:** Kurfürst CO., s.r.o., minerály, drahé kameny, ručně pletené náramky, srdce z kamenů.
- **Wix web:** „KURFÜRST CO., s.r.o.“, Site ID `4e547b0e-3546-40c0-9085-36e85fccbe29`
- **URL:** https://denisschiller2.wixsite.com/kurf-rst-co---s-r-o (zatím bez vlastní domény)
- **Plán:** Free, záměrně. Předplatné (min. **Core**, kvůli platbám) koupím až před spuštěním.
- **Editor:** klasický Wix Editor, Velo zapnuté.
- **Obchod:** Wix Stores **Catalog V3** (jen `/stores/v3/` endpointy), 232 produktů, 24 kategorií.
- **Aplikace:** Instagram Feed, Promote SEO, Wix Chat, Forms & Payments, Hotels, Invoices (V1),
  Pay Links, Multilingual. **Blog není nainstalovaný.**
- Další 2 weby v účtu („Kurfürst CO., s.r.o.“ s ID `57ea19a9-…` a „My Site 1“) jsou staré
  koncepty. **Nesahat na ně.**

---

## 3. Hlavní rozhodnutí

- **Varianta A:** do Vánoc rychlá prodejní verze (produkty, texty, SEO, mobil, začátkem prosince
  předplatné a spuštění prodeje). Velký redesign dotáhneme přes zimu.
- **Reklamy až po spuštění plateb**, jinak se platí za návštěvy, které nemohou nakoupit.
- Dlouhé texty o minerálech jsou v **popisech kategorií**, u produktů jsou krátké popisy.
- URL adresy (slugy) produktů **neměnit**.

---

## 4. Co je hotové

1. **Přejmenování produktů** na unikátní názvy ve formátu
   `Minerál – Lokalita · největší rozměr cm, hmotnost` (174 kamenů). Náramky mají v názvu barvu
   provázku (15 kusů), např. „Ručně pletený náramek s růženínem – vínový provázek“.
2. **Akvamaríny:** lokalita opravena z „Balúčistán“ na **„Gilgit-Baltistán, Pákistán“**
   v názvech i popisech (pákistánské akvamaríny pocházejí ze severu země).
3. **Texty zapsané na web (7. 11. 2026)**, zdroj `texty/navrh-textu-v5.md`, náhled
   https://claude.ai/artifact/5gDUyycpyzZhWx8DUp54fL:
   - **22 kategorií** má popis: pole `description` (max. 600 znaků) = první odstavec,
     pole `richContentDescription` = celý text (formátovaný).
   - **208 produktů** má nový popis: úvodní věta → Lokalita / Rozměry / Hmotnost → „Na fotografii
     je přesně tento kus. Každý kámen je originál.“
   - Náramky mají původní texty (jsou dobré). Srdce mají původní texty + nově uspořádané údaje.
   - Beze změny zůstalo 5 produktů jen s údaji: Spinel – Tanzánie (2×), Zirkon – Norsko,
     Voskový opál/kočičí oko, Azurit (bez šablony textu).
   - **Léčivé účinky** jsou ze všech textů pryč.
4. **Kontrola faktů** původních textů. Opravené hlavní chyby: lokalita rubínu v zoisitu (Mundarara,
   ne Merelani), prasopál je opál (ne chalcedon), nepravdivé využití ametystu v průmyslu,
   „čeští“ misionáři u labradoritu, zeolity u apofylitu a pentagonitu, Kalahari u purpuritu.
5. **Zálohy** ve složce `zalohy/`: původní názvy (4. 11.) a původní popisy všech produktů (7. 11.).

---

## 5. Co čeká na moje potvrzení nebo údaje

- [ ] **3× Prasopál 9 cm / 111 g** (`prasopál-13`, `prasopál-3`, `prasopál-1`): různé kameny,
      nebo omylem zdvojený produkt?
- [ ] **Chybějící údaje:** `prasopál-35` nemá rozměry ani hmotnost, `tanzanit-1` nemá hmotnost.
- [ ] Barvy provázků u fluoritových náramků: jeden „purpurový“, druhý „fialový“. Sedí to?
- [ ] Info: od 4. 11. zmizely 3 produkty (`labradorit-5`, `akvamarín-7`, `akvamarín-2`),
      nejspíš prodané. Jen pro kontrolu.

---

## 6. Co dál (pořadí podle varianty A)

### V editoru (Claude in Chrome)
1. **Ověřit zobrazení popisu kategorie** na stránce kategorie e-shopu. Texty jsou v datech,
   ale klasická šablona je nemusí zobrazovat. Když se nezobrazují, navrhnout, jak je tam dostat.
2. **Zkontrolovat produktové stránky** na počítači i mobilu (vzhled nových popisů).
3. **Audit všech stránek** na počítači i v mobilu, seznam problémů.
4. **Rychlé mobilní úpravy** pro Vánoce a návrh nového vzhledu (2 varianty) ke schválení.

### Přes API
5. **Sjednotit názvy zbylých ~40 produktů** do formátu: překlep „Fuorit“, „Akvapras- Zimbabwe“,
   „Akvapras -Zimbabwe“, „Modrý Chalcedon“, „Růženín -leštěný“, „Spinel - Tanzánie “ (mezera
   na konci), „Fluorit - Kongo/Mexiko/USA/Maroko“ apod.
6. **Zbylé 4 náramky** (sluneční kámen, rubín v zoisitu, čaroit, karneol): doplnit barvu provázku
   z fotek.
7. **Kategorie:** prázdné „Titanit/Sphene“ a „Spessartin“ smazat nebo naplnit,
   „Apofylit a Stilbit“ přejmenovat na „Apofylit a stilbit“.
8. **SEO:** titulky a meta popisy produktů a kategorií, alt texty fotek.
9. **Blog:** nainstalovat Wix Blog. Témata navázaná na prodávané kameny (kámen podle znamení,
   kámen podle měsíce narození, vánoční dárkový průvodce), články s odkazy na produkty.

### Spuštění (začátek prosince)
10. Předplatné (min. **Core**), vlastní doména, platby, doprava, obchodní podmínky.

### Marketing (až po spuštění plateb)
11. Google Search Console a Merchant Center, profil firmy na Googlu, **Heureka a Zboží.cz**,
    Instagram, reklamy, newsletter.

### Nové minerály
12. Mám na skladě nové minerály. Nafotím je, ty napíšeš popisy podle šablony níže, zařadíš je
    do kategorií a nahraješ.

---

## 7. Šablony pro nové produkty

**Název:** `Minerál – Lokalita · největší rozměr cm, hmotnost`
(např. „Fluorit – Loralai, Pákistán · 28 cm, 4,65 kg“; pod 1 kg v gramech, nad 1 kg v kg).

**Popis (HTML do `plainDescription`):**
```html
<p>[1–2 věty o kameni, podle „Úvodní věty“ v texty/navrh-textu-v5.md]</p>
<p>&nbsp;</p>
<p><strong>Lokalita:</strong> Haneti, Tanzanie</p>
<p><strong>Rozměry:</strong> 14 × 7 × 6 cm (š × v × h)</p>
<p><strong>Hmotnost:</strong> 703 g</p>
<p>&nbsp;</p>
<p>Na fotografii je přesně tento kus. Každý kámen je originál.</p>
```

---

## 8. Technické poznámky

- **Produkty (V3):** čtení `POST https://www.wixapis.com/stores/v3/products/query`
  (`fields: ["PLAIN_DESCRIPTION"]`, `cursorPaging`, max. 100). Hromadná úprava
  `POST https://www.wixapis.com/stores/v3/bulk/products/update`
  (`products: [{ product: { id, revision, name?, plainDescription? } }]`, max. 100 na dávku,
  vždy aktuální `revision`). Název max. 80 znaků. `plainDescription` přijímá HTML.
- **Kategorie:** `POST https://www.wixapis.com/categories/v1/categories/query` a
  `PATCH https://www.wixapis.com/categories/v1/categories/{id}` s
  `treeReference: { appNamespace: "@wix/stores" }`. `description` je prostý text (max. 600),
  `richContentDescription` je Ricos dokument (odstavce, BOLD/ITALIC dekorace).
- **Zálohy:** velké odpovědi API se ukládají do souboru. Zálohu dělej po částech (~120 produktů).
- **Fotky produktů** jsou na `static.wixstatic.com`. V cloudu kvůli tomu existuje prostředí
  „Claude“, lokálně to není potřeba.

---

## 9. Jak začít v lokální relaci

1. Naklonuj repozitář `denisschiller2-beep/Claude` a přepni se na větev
   `claude/wix-website-management-etu8bc`.
2. Spusť v té složce Claude Code. Zkontroluj, že je připojený **konektor Wix**
   a rozšíření **Claude in Chrome**.
3. Napiš: *„Přečti si PREDANI-MAC.md a pokračuj bodem 1 v sekci Co dál.“*
