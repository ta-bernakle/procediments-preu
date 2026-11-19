# 📄 Procediment d'impressió de fulls (paper normal / estucat) — v2.2

*(Base per a pressupostos i planificació de comandes: flyers, volants, fulls solts, targetes, etc.)*

---

> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

> 🔄 **CANVI v2.0:** S'incorporen els costos operatius 2026 (`costosOperatius2026.md`). **S'elimina el factor multiplicador de click** de tots els càlculs. El cost d'impressió s'obté directament de la taula `[impressio]` per tipus i mida de màquina.

> 🔧 **CANVI v2.1 (correcció crítica):** S'ha corregit l'error conceptual en el càlcul de fulls físics per a impressions a 2 cares. **El nombre de peces finals que surten d'un SRA3 és SEMPRE `elements_per_full`, independentment de si s'imprimeix a 1 cara, a 2 cares amb contingut igual o a 2 cares amb contingut diferent.** Les cares només afecten el **cost d'impressió** (nombre de clicks), mai el **nombre de fulls SRA3 necessaris** ni el **nombre de peces finals obtingudes**. Vegeu secció 3.2 reescrita.

> 📦 **CANVI v2.2:** S'afegeix el preu real de l'**òfset blanc 300 g = 0,11406 €/full SRA3** (facilitat per l'usuari, preu de factura proveïdor). S'actualitza la taula de materials (secció 7) i s'afegeix una nota sobre la **no-linealitat del preu €/kg** en gramatges alts. Es recalcula l'exemple 5 amb el preu correcte. Es recomana migrar a una taula de cost/full SRA3 directa.

---

## 1\. FULL ESTÀNDARD

-   Mida full base: **320 × 450 mm** (SRA3 / doble foli)
    
-   Vora de seguretat: **8 mm** a cada costat
    
-   Zona útil: **304 × 434 mm**
    
-   Altres formats habituals: A4 (foli), A5 (quartilla), A6 (octavilla), targeta, mini
    
-   Tall: Guillotinat simple (tall complet, sense mitjos talls ni troquelats)
    

---

## 2\. CÀLCUL D'ELEMENTS PER FULL

Per a cada mida d'element, es calculen les dues orientacions i s'escull la que doni més unitats per full.

**Fórmula:**

elements\_ample = part\_entera(zona\_útil\_ample / amplada\_element)
elements\_alt   = part\_entera(zona\_útil\_alt / altura\_element)
total\_per\_full = elements\_ample × elements\_alt

**Exemples:**

| Mida element (mm) | Orientació òptima (ample × alt) | Elements/full SRA3 |
| --- | --- | --- |
| A6 (105 × 148) | 105 × 148 | 8 |
| A5 (148 × 210) | 148 × 210 | 4 |
| A4 (210 × 297) | 210 × 297 | 2 |
| 100 × 150 | 100 × 150 | 8 |
| 90 × 50 | 50 × 90 | 24 |
| 210 × 99 | 210 × 99 | 6 |
| 148 × 105 | 148 × 105 | 8 |
| 150 × 150 | 150 × 150 | 4 |
| 98 × 140 | 98 × 140 | 9 |

---

## 3\. IMPRESSIÓ: 1 CARA / 2 CARES, B/N / COLOR

### 3.1. Tipus d'impressió

| Tipus | Descripció | Observacions |
| --- | --- | --- |
| 1 cara B/N | Només una cara, tinta negra | Cost més baix |
| 2 cares B/N | Dues cares, tinta negra | Cal comptar clicks (2 per full) |
| 1 cara color | Una cara, color | Cost per click color |
| 2 cares color | Dues cares, color | Pot ser color a una o dues cares |
| 2 cares mixt | Una cara B/N i una cara color | Cal desglossar costos |

### 3.2. Càlcul de fulls físics — ⚠️ CORREGIT v2.1

**Regla d'or:** El nombre de **peces finals** que surten d'un full SRA3 és **sempre** `elements_per_full`. El nombre de **fulls SRA3 necessaris** és **sempre**:

fulls\_físics = sostre(unitats\_totals / elements\_per\_full)

**Aquesta fórmula és única i no depèn del nombre de cares.** El tipus d'impressió (1 cara, 2 cares igual, 2 cares diferent) **no canvia mai** el nombre de fulls SRA3 ni el nombre de peces finals. Només canvia el **nombre de clicks** que es facturen (1 o 2 per full).

| Tipus d'impressió | Fulls SRA3 necessaris | Clicks facturats | Peces finals obtingudes |
| --- | --- | --- | --- |
| 1 cara | `sostre(unitats / elements_per_full)` | `fulls × 1` | `fulls × elements_per_full` |
| 2 cares (contingut igual a les dues cares) | `sostre(unitats / elements_per_full)` | `fulls × 2` | `fulls × elements_per_full` |
| 2 cares (contingut diferent a cada cara) | `sostre(unitats / elements_per_full)` | `fulls × 2` | `fulls × elements_per_full` |

> 📌 **Per què és així?** Un full SRA3 té `elements_per_full` posicions. Si hi poses 9 elements de 98×140 mm, sempre en surten 9, tant si imprimeixes una cara com si n'imprimeixes dues. La segona cara no "multiplica" les peces: només afegeix informació al revers de les mateixes 9 peces. Per tant, **mai no es divideix per 2** en el càlcul de fulls.

> ❌ **Error eliminat a v2.1:** La fórmula anterior `sostre(unitats / (elements_per_full × 2))` per a "2 cares amb contingut diferent" era **incorrecta**. Dividia els fulls per 2 com si la segona cara generés peces noves, quan en realitat només imprimeix el revers de les mateixes peces. Això infravalorava el nombre de fulls SRA3 i, per tant, el cost de material i d'impressió.

> ⚠️ **Nota sobre la maculatura:** Si el resultat de `sostre()` deixa peces sobrants (p. ex. 150 unitats amb 9 elements/full → 17 fulls → 153 peces, 3 sobrants), aquestes sobrants **no es poden reaprofitar** per a una altra comanda (el paper ja està tallat i imprès). Es comptabilitzen com a maculatura i el seu cost ja va inclòs en els fulls calculats.

### 3.3. Cost d'impressió (sense factor multiplicador)

El cost d'impressió s'obté directament de `costosOperatius2026.md`, secció `[impressio]`. **No s'aplica cap factor de volum.** El preu per click ja és el cost real per cara impresa segons la màquina i el format.

| Concepte | Cost (€/cara) | Font |
| --- | --- | --- |
| B/N A4 | 0,003147 | `b_n_A4_base` |
| B/N SRA3 | 0,00556 | `b_n_SRA3_base` |
| Color A4 | 0,030426 | `color_A4_base` |
| Color SRA3 | 0,03966 | `color_SRA3_base` |

**Fórmula:**

Cost\_impressió = fulls\_físics × nombre\_de\_cares\_impreses × cost\_click\_per\_cara

On:

-   `fulls_físics` \= `sostre(unitats_totals / elements_per_full)` (secció 3.2)
    
-   `nombre_de_cares_impreses` \= 1 (1 cara) o 2 (2 cares, igual o diferent)
    
-   `cost_click_per_cara` \= segons format físic (SRA3/A4) i tinta (B/N/color)
    

> 📌 **Nota:** El cost de click SRA3 ja inclou la impressió del full sencer (tots els elements que hi caben). Per tant, `fulls_físics` és el nombre de fulls SRA3 que passen per la màquina, i el cost per cara s'aplica un cop per full i per cara.

---

## 4\. GUILLOTINAT

### 4.1. Taula de temps de guillotina per format

Els temps ja inclouen preparació de la guillotina, manipulació, talls, gir de full i canvi de full. No cal afegir res més.

| Format | Quantitat base | Temps base (min) | Increment (min/1.000 unitats) | Quan s'aplica |
| --- | --- | --- | --- | --- |
| Doble foli (SRA3) | 1.000 | 10 | 3,96 | Fulls SRA3 |
| Foli (A4) | 1.000 | 10 | 1,96 | Fulls A4 |
| Quartilla (A5) | 2.000 | 13 | 2,04 | Fulls A5 |
| Octavilla (A6) | 2.000 | 15 | 1,89 | Fulls A6 |
| Mitja octavilla (targeta) | 2.000 | 20 | 2,24 | Targetes ≥ 85 × 55 mm |
| Etiqueta mini | 2.000 | 30 | 2,14 | Elements < 85 × 55 mm |

> 📌 **Nota v2.1:** La "Quantitat" d'aquesta taula es refereix al **nombre de fulls SRA3** que es guillotinen, no al nombre de peces finals. El guillotinat es fa sobre els fulls SRA3 (secció 3.2).

### 4.2. Fórmula

Temps\_guillotina (min) = Temps\_base + (fulls\_físics − Quantitat\_base) / 1.000 × Increment

Si `fulls_físics` és inferior a la quantitat base → s'agafa el temps base.

Cost\_guillotina = Temps\_guillotina / 60 × 27,78 €/h

### 4.3. Exemple

Comanda: 5.000 flyers A5 (quartilla) → 5.000/4 = 1.250 fulls SRA3

Temps = 13 + (1.250 − 2.000) / 1.000 × 2,04 → fulls < base → 13 min
Cost = 13 / 60 × 27,78 = 6,02 €

> ⚠️ **Correcció v2.1:** L'exemple original agafava 5.000 peces com a "quantitat" per a la taula, però la taula de guillotina es refereix a **fulls SRA3**. Amb 5.000 A5 calen 1.250 fulls SRA3, que estan per sota de la base de 2.000 → temps base 13 min. L'original deia 19,12 min perquè comptava 5.000 peces. **Corregit.**

---

## 5\. ESTRUCTURA DE COSTOS (v2.2)

| Partida | Càlcul / Base | Font |
| --- | --- | --- |
| Material | €/full × fulls\_físics | `[paper_full_sra3]` (recomanat) o `[paper]` × àrea SRA3 (0,144 m²) |
| Impressió | €/click × fulls\_físics × nombre\_de\_cares | `[impressio]` (sense factor) |
| Preimpressió | 15 min base (33,08 €/h) + 5 min/model addicional | `[ma_d_obra] preparacio_imposicio` |
| Guillotinat | Taula de temps per format × 27,78 €/h (sobre fulls SRA3) | `[ma_d_obra] guillotinat` |
| Empaquetat + transport | 6 € base + 1,5 min per model (19,93 €/h) | `[ma_d_obra] manipulat_empaquetat` + `[operatius] transport_per_comanda` |

> ❌ **Eliminat:** Taula de factors de correcció d'impressió (×30, ×25, ×20, ×18, ×16, ×15, ×12, ×10). Ja no s'aplica cap multiplicador al click.

> ⚠️ **Nou v2.2:** Es recomana usar la taula `[paper_full_sra3]` (cost directe per full SRA3) en lloc de la fórmula lineal `€/kg × gramatge × 0,144 m²`, perquè **la relació €/kg no és lineal amb el gramatge** (els papers gruixuts tenen preu/kg més alt). Vegeu secció 7.

---

## 6\. EXEMPLES PRÀCTICS (v2.2 — recalculats)

### Exemple 1: 500 flyers A6 (105×148 mm), 1 cara color, paper estucat 135 g

-   Elements/full: 8 → fulls físics = sostre(500/8) = **63 fulls SRA3**
    
-   Material: 63 × 0,03402 € = **2,14 €**
    
-   Impressió: 63 × 1 cara × 0,03966 €/cara SRA3 = **2,50 €**
    
-   Preimpressió: 15 min = **8,27 €**
    
-   Guillotinat: 15 min (base, 63 < 2.000) = **6,95 €**
    
-   Empaq.+transp.: **6,00 €**
    

| Partida | Import |
| --- | --- |
| Material | 2,14 € |
| Impressió (1 cara) | 2,50 € |
| Preimpressió | 8,27 € |
| Guillotinat | 6,95 € |
| Empaq.+transp. | 6,00 € |
| **COST BASE** | **25,86 €** |
| €/flyer | **0,052 €** |

---

### Exemple 2: 1.000 flyers A5 (148×210 mm), 2 cares color, paper estucat 135 g

-   Elements/full: 4 → fulls físics = sostre(1.000/4) = **250 fulls SRA3**
    
-   Material: 250 × 0,03402 € = **8,51 €**
    
-   Impressió: 250 × 2 cares × 0,03966 € = **19,83 €**
    
-   Preimpressió: 15 min = **8,27 €**
    
-   Guillotinat: 13 min (base, 250 < 2.000) = **6,02 €**
    
-   Empaq.+transp.: **6,00 €**
    

| Partida | Import |
| --- | --- |
| Material | 8,51 € |
| Impressió (2 cares) | 19,83 € |
| Preimpressió | 8,27 € |
| Guillotinat | 6,02 € |
| Empaq.+transp. | 6,00 € |
| **COST BASE** | **48,63 €** |
| Marge 50% | 24,32 € |
| **PREU VENDA** | **72,95 €** |
| €/flyer | **0,073 €** |

---

### Exemple 3: 10.000 flyers A6 (148,5×105 mm), 1 cara B/N, paper òfset blanc 80 g

-   Elements/full: 8 → fulls físics = sostre(10.000/8) = **1.250 fulls SRA3**
    
-   Material: 1.250 × 0,01774 € = **22,18 €**
    
-   Impressió B/N: 1.250 × 1 cara × 0,00556 € = **6,95 €**
    
-   Preimpressió: 15 min = **8,27 €**
    
-   Guillotinat: taula A6, fulls 1.250 < 2.000 → **15 min** \= **6,95 €**
    
-   Empaq.+transp.: **6,50 €**
    

| Partida | Import |
| --- | --- |
| Material | 22,18 € |
| Impressió (B/N, 1 cara) | 6,95 € |
| Preimpressió | 8,27 € |
| Guillotinat | 6,95 € |
| Empaq.+transp. | 6,50 € |
| **COST BASE** | **50,85 €** |
| €/flyer | **0,0051 €** |

---

### Exemple 4: 250 targetes (85×55 mm), 2 cares B/N, paper normal 80 g

-   Elements/full: orientació òptima 55×85 → ample ⌊304/55⌋=5, alt ⌊434/85⌋=5 → **25 elements/full**
    
-   Fulls físics: sostre(250/25) = **10 fulls SRA3**
    
-   Material: 10 × 0,01774 € = **0,18 €**
    
-   Impressió B/N: 10 × 2 cares × 0,00556 € = **0,11 €**
    
-   Preimpressió: 15 min = **8,27 €**
    
-   Guillotinat: 20 min (base, 10 < 2.000) = **9,26 €**
    
-   Empaq.+transp.: **6,00 €**
    

| Partida | Import |
| --- | --- |
| Material | 0,18 € |
| Impressió (B/N, 2 cares) | 0,11 € |
| Preimpressió | 8,27 € |
| Guillotinat | 9,26 € |
| Empaq.+transp. | 6,00 € |
| **COST BASE** | **23,82 €** |
| €/targeta | **0,095 €** |

---

### Exemple 5: 150 impresos 98×140 mm, 2 cares color (4+4), òfset blanc 300 g

-   Elements/full: orientació òptima 98×140 → ample ⌊304/98⌋=3, alt ⌊434/140⌋=3 → **9 elements/full**
    
-   Fulls físics: sostre(150/9) = **17 fulls SRA3** (17 × 9 = 153 peces → 3 sobrants de maculatura)
    
-   Material: 17 × **0,11406 €** \= **1,94 €** *(preu real v2.2)*
    
-   Impressió: 17 × 2 cares × 0,03966 € = **1,35 €**
    
-   Preimpressió (35 min): 35/60 × 33,08 = **19,30 €**
    
-   Guillotinat: 10 min (base, 17 < 1.000) = **4,63 €**
    
-   Empaq.+transp.: **6,00 €**
    

| Partida | Import |
| --- | --- |
| Material | 1,94 € |
| Impressió (4+4, 2 cares) | 1,35 € |
| Preimpressió + maquetació | 19,30 € |
| Guillotinat | 4,63 € |
| Empaq.+transp. | 6,00 € |
| **COST BASE** | **33,22 €** |
| €/impreso | **0,221 €** |

> ✅ **Correcció v2.2:** El material s'ha recalculat amb el preu real de l'òfset 300 g (**0,11406 €/full SRA3**), no amb la fórmula lineal €/kg. El cost base puja de 32,41 € a **33,22 €**. Amb marge 130%: **76,41 €** (0,509 €/unitat). Arrodoniment comercial: **77 €**.

---

## 7\. MATERIALS DISPONIBLES (preus / full SRA3) — v2.2

### 7.1. Taula recomanada: cost directe per full SRA3

**Aquesta és la taula que s'ha de fer servir per a pressupostos.** Preus de factura proveïdor per full SRA3 (320×450 mm).

| Material | Gramatge | Cost/full SRA3 | Font |
| --- | --- | --- | --- |
| Ofset blanc 70 g | 70 | 0,01593 € | `[paper]` (lineal) |
| Ofset blanc 80 g | 80 | 0,01774 € | `[paper]` (lineal) |
| **Ofset 140 g** | **140** | **0,03105 €** | `[paper]` (lineal) |
| Ofset blanc 160 g | 160 | 0,03686 € | `[paper]` (lineal) |
| **Ofset blanc 300 g** | **300** | **0,11406 €** | ✅ **Preu real proveïdor (v2.2)** |
| Ofset blanc 350 g | 350 | 0,08064 € | `[paper]` (lineal) — ⚠️ revisar |
| Estucat 115 g | 115 | 0,02898 € | `[paper]` (lineal) |
| Estucat 135 g | 135 | 0,03402 € | `[paper]` (lineal) |
| Estucat 170 g | 170 | 0,04284 € | `[paper]` (lineal) |
| Estucat 250 g | 250 | 0,06840 € | `[paper]` (lineal) |
| Estucat 300 g | 300 | 0,08208 € | `[paper]` (lineal) — ⚠️ revisar |
| Estucat 350 g | 350 | 0,09576 € | `[paper]` (lineal) |
| Kraftliner 275 g | 275 | 0,05921 € | `[paper]` (lineal) |
| Folding 275 g | 275 | 0,06534 € | `[paper]` (lineal) |

> ⚠️ **Atenció v2.2:** La fórmula lineal `€/kg × gramatge × 0,144 m²` **no és fiable per a gramatges alts**. L'òfset 300 g real és **0,11406 €/full** (≈2,64 €/kg), molt lluny del que donaria la fórmula amb 1,54 €/kg (0,06653 €). **Cal revisar tots els preus amb factures reals del proveïdor** i substituir la taula lineal per cost/full directe.

### 7.2. Taula històrica: €/kg (només referència)

| Material | €/kg | Font |
| --- | --- | --- |
| Ofset 70 g | 1,58 | `[paper] ofset_70` |
| Ofset 80 g | 1,54 | `[paper] ofset_80` |
| Ofset 140 g | 1,54 | `[paper] ofset_140` |
| Ofset 160 g | 1,60 | `[paper] ofset_160` |
| Ofset 350 g | 1,60 | `[paper] ofset_350` |
| Estucat 115 g | 1,75 | `[paper] estucat_115` |
| Estucat 135 g | 1,75 | `[paper] estucat_135` |
| Estucat 170 g | 1,75 | `[paper] estucat_170` |
| Estucat 250 g | 1,90 | `[paper] estucat_250` |
| Estucat 300 g | 1,90 | `[paper] estucat_300` |
| Estucat 350 g | 1,90 | `[paper] estucat_350` |
| Kraftliner 275 g | 1,495 | `[paper] kraftliner_275` |
| Folding 275 g | 1,65 | `[paper] folding_275` |

> 📌 **Nota:** Aquesta taula es manté com a referència històrica i per a càlculs d'altres formats (A4, etc.), però **per a pressupostos de flyers/cartells en SRA3 s'ha d'usar la taula 7.1** (cost directe per full).

**Proposta d'estructura per a `costosOperatius2026.md`:**

\[paper\_full\_sra3\]
\# Cost real per full SRA3 (320x450 mm) — preu de factura proveïdor
ofset\_70    \= 0.0xxxx
ofset\_80    \= 0.0xxxx
ofset\_140   \= 0.0xxxx
ofset\_160   \= 0.0xxxx
ofset\_300   \= 0.11406   # <-- preu real proveïdor (v2.2)
ofset\_350   \= 0.0xxxx
estucat\_115 \= 0.0xxxx
estucat\_135 \= 0.0xxxx
estucat\_170 \= 0.0xxxx
estucat\_250 \= 0.0xxxx
estucat\_300 \= 0.0xxxx   # <-- revisar
estucat\_350 \= 0.0xxxx
kraftliner\_275 \= 0.0xxxx
folding\_275    \= 0.0xxxx

---

## 8\. NOTES PER A FUTURES COMANDES

-   Sempre calcular les dues orientacions de l'element.
    
-   **El nombre de fulls SRA3 és SEMPRE `sostre(unitats_totals / elements_per_full)`. Mai no es divideix per 2, ni per cap altre factor, en funció de les cares.** Les cares només afecten els clicks facturats.
    
-   **El nombre de peces finals que surten d'un SRA3 és SEMPRE `elements_per_full`**, independentment de si s'imprimeix a 1 cara, 2 cares igual o 2 cares diferent.
    
-   Per a 2 cares, l'única diferència és que es facturen **2 clicks per full** en lloc d'1.
    
-   **Impressió: usar directament el cost de `[impressio]` de `costosOperatius2026.md`. No aplicar cap factor multiplicador.**
    
-   Per a B/N, usar `b_n_SRA3_base` o `b_n_A4_base` segons el full físic.
    
-   Per a color, usar `color_SRA3_base` o `color_A4_base` segons el full físic.
    
-   **Guillotinat: la "Quantitat" de la taula es refereix a fulls SRA3, no a peces finals.**
    
-   Si `fulls_físics` és inferior a la quantitat base de la taula → agafar el temps base.
    
-   Si l'element és inferior a 85 × 55 mm, aplicar la taula mini.
    
-   **Material: usar preferentment la taula `[paper_full_sra3]` (cost directe per full). Si no hi és, usar `[paper]` (€/kg) com a referència, però revisar el resultat per a gramatges alts.**
    
-   Paper de color: demanar preu actualitzat en el moment del pressupost.
    
-   Paper no tabulat: demanar preu al proveïdor o usar el més proper com a referència, mai inventar-lo.
    
-   **Revisar el marge comercial:** sense factor de click, les tirades grans surten molt més barates. Cal assegurar que el marge cobreixi costos indirectes i benefici.
    
-   Guardar aquest document com a referència per a futures consultes.
    

---

📌 **Versió:** 2.2  
📅 **Data:** 2026-11-18  
✏️ **Canvis v2.2:** Afegit preu real de l'òfset blanc 300 g (0,11406 €/full SRA3). Actualitzada la taula de materials (secció 7) amb taula recomanada de cost/full directe i taula històrica €/kg. Recalculat exemple 5 (cost base 33,22 €, preu venda 76,41 € amb marge 130%). Afegida nota sobre no-linealitat del preu €/kg en gramatges alts. Proposada estructura `[paper_full_sra3]` per a `costosOperatius2026.md`.  
🔄 **Pendent:** revisar tots els preus de paper amb factures reals del proveïdor i substituir la taula lineal per cost/full directe. Validar marges comercials sense factor de click amb casos històrics.
