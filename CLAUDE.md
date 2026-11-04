# Projekt Kurfürst CO. – paměť projektu pro Clauda

Tento soubor si Claude Code načte automaticky na začátku každé relace v tomto repozitáři.
Díky tomu nová relace hned ví, na čem pracujeme, a nemusíme vše vysvětlovat znovu.
**Po každém větším kroku ho aktualizuj** (sekce „Stav“ a „Deník rozhodnutí“).

## O projektu

- Firma: **Kurfürst CO., s.r.o.**, e-shop s minerály, drahými kameny a ručně dělanými šperky
  (pletené náramky s kameny, srdce z minerálů, surové a tromlované kameny).
- Cíl: předělat a zmodernizovat web, plně responzivní (mobil!), doplnit nové minerály ze skladu,
  SEO + Google, blog o minerálech, Instagram, reklamy, newsletter, a hlavně **objednávky**.

## Wix web (hlavní a jediný, na kterém pracujeme)

| Údaj | Hodnota |
|---|---|
| Název | KURFÜRST CO., s.r.o. |
| Site ID | `4e547b0e-3546-40c0-9085-36e85fccbe29` |
| URL | https://denisschiller2.wixsite.com/kurf-rst-co---s-r-o |
| Plán | **Free** (zatím bez předplatného, záměrně až po předělávce) |
| Editor | Wix Editor (klasický), Velo zapnuté |
| Wix Stores | **Catalog V3**: používat jen `/stores/v3/` endpointy |
| Jazyk / měna | cs, CZK, Europe/Prague; nainstalovaný Wix Multilingual |
| Další aplikace | Instagram Feed, Promote SEO, Wix Chat, Forms & Payments, Hotels, Invoices (V1), Pay Links |
| Blog | **Zatím není nainstalovaný** |

Další dva weby v účtu („Kurfürst CO., s.r.o.“ s ID `57ea19a9-…` a „My Site 1“) jsou staré
nezveřejněné koncepty z 2/2023. **Nesahat na ně.**

### Důležité k předplatnému

Podle Wix Help Center lze obchod nastavit zdarma, ale **přijímat platby jde až od plánu Core výš**
(plán Light platby neumí). Předplatné tedy kupovat až těsně před ostrým spuštěním.

## Pravidla spolupráce

1. Komunikace **česky**. **Odpovědi stručně, jen důležité info** (majitel nechce číst dlouhé texty).
   „Proč“ vysvětlit jednou větou, jen když je to potřeba.
2. **Nic se nepublikuje na živý web bez schválení majitele.** Claude připraví, pošle náhled
   a majitel schválí. Hromadné e-maily (newsletter) odesílá vždy majitel.
3. Data (produkty, blog, SEO, kontakty) se mění přes **Wix API**. Vzhled a rozložení se mění
   v **editoru** přes Claude in Chrome / computer use na Macu majitele.
4. Před změnou vzhledu nejdřív návrh (barvy, fonty, struktura), po schválení realizace.
5. Snažit se vždy najít řešení. Když jedna cesta nejde, navrhnout jinou.

## Stav: audit produktů (4. 11. 2026)

- **235 produktů**, všechny viditelné, všechny mají fotku i kategorii (24 kategorií), 14 vyprodaných.
- ⚠️ **193 produktů sdílí stejný název s jinými**, např. 27× „Prasopál“, 22× „Fluorit“,
  21× „Labradorit“, 20× „Ametyst“, 20× „Rubín v zoisitu“, 19× „Akvapras – Zimbabwe“.
  Pro Google to znamená desítky stránek se stejným titulkem (soupeří spolu ve vyhledávání)
  a zákazník je od sebe nerozliší. → Přejmenovat na unikátní názvy (tvar, velikost, váha, původ).
- Popisy jsou krátké (medián ~105 znaků) → rozšířit kvůli SEO a důvěře zákazníka.

## Plán (roadmapa)

**Platí varianta A (viz Deník):** nejdřív vánoční minimum (body 3, část 6 a 5), pak redesign přes zimu.

1. **Audit** webu: struktura stránek, mobilní zobrazení, rychlost, SEO, produkty (produkty hotové).
2. **Návrh nového vzhledu** → schválení → realizace v editoru (důraz na mobil).
3. **Produkty**: unikátní názvy, delší popisy, SEO titulky a alt texty; nové minerály ze skladu
   (majitel nafotí, Claude napíše popisy, zařadí do kategorií a nahraje).
4. **Blog o minerálech**: nainstalovat Wix Blog, témata navázaná na prodávané kameny,
   články s odkazy na produkty.
5. **Spuštění**: předplatné (min. Core), vlastní doména, platby, doprava, obchodní podmínky.
6. **Marketing**: Google Search Console + Merchant Center, Instagram, reklamy, newsletter.
   Reklamy až po spuštění plateb, jinak se platí za návštěvy, které nemohou nakoupit.

### Přejmenování produktů: rozbor (4. 11. 2026)

- Popisy kamenů mají jednotnou strukturu `Lokalita: … Rozměry (cm - š-v-h): … Hmotnost (g): …`,
  takže unikátní název jde sestavit automaticky u **176 ze 193** duplicitních produktů.
- Formát: `Minerál – Lokalita · největší rozměr cm, hmotnost` (schváleno majitelem).
- ✅ **Hotovo 4. 11. 2026: přejmenováno 174 produktů** (0 chyb). Záloha původních názvů:
  `zalohy/2026-11-04-puvodni-nazvy-produktu.json`. U `akvapras-zimbabwe-8` je v popisu
  překlep „Lokalita: Akvapras“, v názvu je správně Zimbabwe (popis ještě opravit).
- Náramky: každý má jiný minerál a **jinou barvu provázku** (info od majitele) → do názvu
  přidat barvu provázku. Fotky z `static.wixstatic.com` jsou síťovou politikou prostředí
  blokované, takže barvy buď dodá majitel, nebo povolí doménu v nastavení prostředí.
- Bez dat (nutný vstup majitele): 15 pletených náramků (popis bez rozměrů), `prasopál-35`
  (prázdné rozměry i hmotnost), `tanzanit-1` (chybí hmotnost).
- Podezření na omylem zdvojený produkt: 3× „Prasopál“ se stejnými údaji 9 cm / 111 g.
- Nejednotné lokality (Tanzania/Tanzanie, Mundara/Mundarara mine, Pakistan/Pákistán, Mexico…)
  → sjednotit česky.
- Nekonzistence v názvech: „Tanzanit “ a „Kalcit, apofylit & stilbit “ s mezerou na konci,
  „Rubín v Zoisitu“ vs. „Rubín v zoisitu“.
- Slugy (URL) zatím neměnit, aby nevznikly nefunkční odkazy. Před přejmenováním uložit
  zálohu původních názvů.

## Čeká na majitele

- Povolit síť pro `static.wixstatic.com` (na Macu přes claude.ai/code, na iPadu nastavení nejde otevřít).
- Odpověď: 3× prasopál 9 cm / 111 g (`prasopál-13`, `-3`, `-1`) jsou různé kameny, nebo duplikát?

## Deník rozhodnutí

- 2026-11-04: Hlavní web je KURFÜRST CO., s.r.o. (235 produktů). Předplatné až po předělávce.
- 2026-11-04: Zvolena **varianta A**: rychlá vánoční verze (oprava produktů, SEO, mobil,
  začátkem prosince předplatné a spuštění prodeje). Velký redesign dotáhneme přes zimu.
