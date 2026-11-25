# 

# CÀLCUL DE COSTOS D'IMPRESSIÓ I PAPER PER A TALONARIS DE PAPER QUÍMIC

## Versió 2.0 — Data: 2026-06-05

---

## 0\. NOTES PRÈVIES I MARGE COMERCIAL

> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment **NO inclou costos indirectes** (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica **sobre el cost de producció** i ha de cobrir aquests costos indirectes a més del benefici net.
> 
> Es recomana revisar el marge segons el volum de la comanda:
> 
> -   **100–150%** per a comandes petites
>     
> -   **75–100%** per a comandes mitjanes
>     
> -   **50–75%** per a comandes grans
>     
> -   **25–50%** per a comandes molt grans
>     
> 
> Alternativament, es pot usar **marge sobre preu de venda** en lloc de marge sobre cost.

> 🔄 **CANVI v2.0:** S'elimina el factor multiplicador de click (×6, ×4, ×3). El cost d'impressió s'obté directament de `costosOperatius2026.md` (`color_SRA3_base = 0,03966 €/cara`). S'unifiquen guillotinat, preparació, empaquetat i transport amb el procediment de flyers v2.2. S'afegeix nota completa de marge comercial i secció de notes per a futures comandes.

---

## 1\. DADES DE PARTIDA

| Concepte | Valor |
| --- | --- |
| Format d'impressió | SRA3 (320 × 450 mm) |
| Relació SRA3 / mida final | DIN A-4: 1 SRA3 = 2 unitats · DIN A-5: 1 SRA3 = 4 unitats |

**Paper químic (preus per full SRA3):**

| Full | Color | Preu (€/full SRA3) |
| --- | --- | --- |
| 1r full | Blanc (només rep) | 0,1154 |
| 2n full | Blau (rep i copia) | 0,1390 |
| 3r full | Groc (només rep) | 0,1027 |

---

## 2\. COSTOS D'IMPRESSIÓ (€/cara SRA3)

| Tipus | Cost per cara SRA3 | Factor corrector | Cost efectiu |
| --- | --- | --- | --- |
| Blanc i negre | 0,003061 € | ×8 (fix) | 0,024488 € |
| Color | 0,03966 € (de `costosOperatius2026.md`) | ×2 a ×4 (segons criteri) | 0,07932 – 0,15864 € |

**Nota:** Els factors correctors compensen parades de màquina i reposició de components. Per a blanc i negre és fix ×8. Per a color es recomana entre ×2 i ×4 segons la complexitat.

---

## 3\. TEMPS DE PREPARACIÓ

| Concepte | Temps | Cost/hora |
| --- | --- | --- |
| Preparació base (imposició, etc.) | 15 min | 33,08 €/h |
| Preparació amb numeració | 30 min | 33,08 €/h |

---

## 4\. GUILLOTINAT PREVI (tallar SRA3 a mida final)

| Concepte | Temps | Cost/hora |
| --- | --- | --- |
| Preparació guillotina | 5 min (fix per comanda) | 27,78 €/h |
| Tall per cada 500 fulls | 3 min | 27,78 €/h |
| Temps mínim total | 10 min | 27,78 €/h |

---

## 5\. MACULATURA (per comanda i model)

| Concepte | Unitats |
| --- | --- |
| Maculatura estàndard (segons `costosOperatius2026.md`) | 4 unitats per model |

---

## 6\. FÓRMULES DE CÀLCUL

### 6.1. Nombre de fulls SRA3 a imprimir

Per a una comanda de **N** talonaris:

1.  **Fulls per talonari** \= nombre de còpies × 50 jocs
    
    -   Duplicat (2 còpies): 100 fulls/talonari
        
    -   Triplicat (3 còpies): 150 fulls/talonari
        
2.  **Total fulls mida final sense maculatura** \= N × fulls\_per\_talonari
    
3.  **Total fulls SRA3 sense maculatura** \= total\_fulls\_mida\_final / unitats\_per\_SRA3
    
    -   DIN A-4: unitats\_per\_SRA3 = 2
        
    -   DIN A-5: unitats\_per\_SRA3 = 4
        
4.  **Total fulls SRA3 amb maculatura** \= total\_fulls\_SRA3\_sense\_maculatura + maculatura (4 unitats)
    

### 6.2. Cost de paper

Cost paper = (total\_fulls\_SRA3\_amb\_maculatura / nombre\_de\_còpies) × (suma\_preus\_cada\_color)

On `nombre_de_còpies` és 2 (duplicat) o 3 (triplicat).

**Exemple per a 10 talonaris DIN A-4 duplicats:**

-   Fulls per talonari = 2 × 50 = 100 fulls
    
-   Total fulls mida final = 10 × 100 = 1.000 fulls
    
-   Total fulls SRA3 = 1.000 / 2 = 500 fulls
    
-   Amb maculatura = 500 + 4 = 504 fulls SRA3
    
-   Cost paper = (504 / 2) × (0,1154 + 0,1027) = 252 × 0,2181 = **54,96 €**
    

### 6.3. Cost d'impressió

Cost impressió = total\_fulls\_SRA3\_amb\_maculatura × cares\_per\_full × cost\_cara\_efectiu

-   1 cara (només una cara impresa): `cares_per_full = 1`
    
-   2 cares (doble cara): `cares_per_full = 2`
    

**Exemple (continuació):**

-   Impressió B/N 1 cara: 504 × 1 × 0,024488 = **12,34 €**
    

### 6.4. Cost de preparació

Cost preparació = (minuts\_preparacio / 60) × 33,08

-   Sense numeració: 15 minuts → **8,27 €**
    
-   Amb numeració: 30 minuts → **16,54 €**
    

### 6.5. Cost de guillotinat previ

Cost guillotinat = max(10 min, 5 min + (total\_fulls\_SRA3\_amb\_maculatura / 500) × 3 min) / 60 × 27,78

**Exemple (continuació):**

-   504 fulls → 5 + (504/500)×3 = 5 + 3,02 = 8,02 min → max(10, 8,02) = 10 min
    
-   Cost = (10/60) × 27,78 = **4,63 €**
    

### 6.6. Cost total d'impressió i paper

Cost total = cost\_paper + cost\_impressió + cost\_preparació + cost\_guillotinat

**Exemple (continuació):**

-   54,96 + 12,34 + 8,27 + 4,63 = **80,20 €**
    

---

## 7\. INSTRUCCIONS D'ÚS

Per calcular el cost d'impressió i paper d'una comanda, cal especificar:

1.  Mida final del talonari: DIN A-4 o DIN A-5
    
2.  Tipus de talonari: duplicat (2 còpies) o triplicat (3 còpies)
    
3.  Nombre de talonaris (N)
    
4.  Tipus d'impressió: blanc i negre o color
    
5.  Cares a imprimir: 1 cara o 2 cares
    
6.  Numeració: sí o no (afecta el temps de preparació)
    
7.  Factor corrector per a color: 2×, 3× o 4× (segons criteri)
    

---

## 8\. TAULES DE RESULTATS PER A DIFERENTS TIRADES

### 8.1. DIN A-4 — Duplicat — B/N 1 cara — Sense numeració

| N (talonaris) | Fulls SRA3 | Paper (€) | Impressió (€) | Preparació (€) | Guillotinat (€) | TOTAL (€) |
| --- | --- | --- | --- | --- | --- | --- |
| 4 | 204 | 22,25 | 5,00 | 8,27 | 4,63 | 40,15 |
| 10 | 504 | 54,96 | 12,34 | 8,27 | 4,63 | 80,20 |
| 15 | 754 | 82,24 | 18,46 | 8,27 | 5,70 | 114,67 |
| 20 | 1.004 | 109,51 | 24,59 | 8,27 | 6,77 | 149,14 |
| 25 | 1.254 | 136,78 | 30,71 | 8,27 | 7,85 | 183,61 |
| 30 | 1.504 | 164,05 | 36,83 | 8,27 | 8,92 | 218,07 |
| 35 | 1.754 | 191,32 | 42,95 | 8,27 | 9,99 | 252,53 |
| 40 | 2.004 | 218,59 | 49,07 | 8,27 | 11,06 | 286,99 |
| 45 | 2.254 | 245,86 | 55,20 | 8,27 | 12,13 | 321,46 |
| 50 | 2.504 | 273,13 | 61,32 | 8,27 | 13,20 | 355,92 |
| 100 | 5.004 | 545,87 | 122,54 | 8,27 | 24,76 | 701,44 |

### 8.2. DIN A-4 — Triplicat — B/N 1 cara — Sense numeració

| N (talonaris) | Fulls SRA3 | Paper (€) | Impressió (€) | Preparació (€) | Guillotinat (€) | TOTAL (€) |
| --- | --- | --- | --- | --- | --- | --- |
| 4 | 304 | 36,20 | 7,44 | 8,27 | 4,63 | 56,54 |
| 10 | 754 | 89,79 | 18,46 | 8,27 | 5,70 | 122,22 |
| 15 | 1.129 | 134,44 | 27,65 | 8,27 | 7,21 | 177,57 |
| 20 | 1.504 | 179,08 | 36,83 | 8,27 | 8,92 | 233,10 |
| 25 | 1.879 | 223,73 | 46,01 | 8,27 | 10,64 | 288,65 |
| 30 | 2.254 | 268,38 | 55,20 | 8,27 | 12,13 | 343,98 |
| 35 | 2.629 | 313,03 | 64,38 | 8,27 | 13,85 | 399,53 |
| 40 | 3.004 | 357,68 | 73,56 | 8,27 | 15,57 | 455,08 |
| 45 | 3.379 | 402,33 | 82,74 | 8,27 | 17,28 | 510,62 |
| 50 | 3.754 | 446,98 | 91,93 | 8,27 | 18,99 | 566,17 |
| 100 | 7.504 | 893,48 | 183,76 | 8,27 | 37,08 | 1.122,59 |

### 8.3. DIN A-5 — Duplicat — B/N 1 cara — Sense numeració

| N (talonaris) | Fulls SRA3 | Paper (€) | Impressió (€) | Preparació (€) | Guillotinat (€) | TOTAL (€) |
| --- | --- | --- | --- | --- | --- | --- |
| 4 | 104 | 11,34 | 2,55 | 8,27 | 4,63 | 26,79 |
| 10 | 254 | 27,70 | 6,22 | 8,27 | 4,63 | 46,82 |
| 15 | 379 | 41,33 | 9,28 | 8,27 | 4,63 | 63,51 |
| 20 | 504 | 54,96 | 12,34 | 8,27 | 4,63 | 80,20 |
| 25 | 629 | 68,59 | 15,40 | 8,27 | 5,16 | 97,42 |
| 30 | 754 | 82,24 | 18,46 | 8,27 | 5,70 | 114,67 |
| 35 | 879 | 95,87 | 21,52 | 8,27 | 6,23 | 131,89 |
| 40 | 1.004 | 109,51 | 24,59 | 8,27 | 6,77 | 149,14 |
| 45 | 1.129 | 123,14 | 27,65 | 8,27 | 7,21 | 166,27 |
| 50 | 1.254 | 136,78 | 30,71 | 8,27 | 7,85 | 183,61 |
| 100 | 2.504 | 273,13 | 61,32 | 8,27 | 13,20 | 355,92 |

### 8.4. DIN A-5 — Triplicat — B/N 1 cara — Sense numeració

| N (talonaris) | Fulls SRA3 | Paper (€) | Impressió (€) | Preparació (€) | Guillotinat (€) | TOTAL (€) |
| --- | --- | --- | --- | --- | --- | --- |
| 4 | 154 | 18,34 | 3,77 | 8,27 | 4,63 | 35,01 |
| 10 | 379 | 45,12 | 9,28 | 8,27 | 4,63 | 67,30 |
| 15 | 569 | 67,74 | 13,93 | 8,27 | 4,63 | 94,57 |
| 20 | 754 | 89,79 | 18,46 | 8,27 | 5,70 | 122,22 |
| 25 | 944 | 112,41 | 23,12 | 8,27 | 6,50 | 150,30 |
| 30 | 1.129 | 134,44 | 27,65 | 8,27 | 7,21 | 177,57 |
| 35 | 1.319 | 157,07 | 32,30 | 8,27 | 8,01 | 205,65 |
| 40 | 1.504 | 179,08 | 36,83 | 8,27 | 8,92 | 233,10 |
| 45 | 1.694 | 201,70 | 41,48 | 8,27 | 9,73 | 261,18 |
| 50 | 1.879 | 223,73 | 46,01 | 8,27 | 10,64 | 288,65 |
| 100 | 3.754 | 446,98 | 91,93 | 8,27 | 18,99 | 566,17 |

---

## 9\. INSTRUCCIONS PER A COLOR

Per a impressions en color, s'aplica un factor corrector de 2× a 4× sobre el cost base de **0,03966 €/cara SRA3** (de `costosOperatius2026.md`).

**Recomanació:**

-   Impressió simple (pocs colors, poc cobriment): **2×** → 0,07932 €/cara
    
-   Impressió mitjana: **3×** → 0,11898 €/cara
    
-   Impressió complexa (alta cobertura, fotografies): **4×** → 0,15864 €/cara
    

**Exemple:** 10 talonaris DIN A-4 duplicats, color 1 cara, factor 3×:

-   Cost impressió = 504 × 1 × (0,03966 × 3) = 504 × 0,11898 = **59,97 €**
    
-   Total = paper (54,96) + impressió (59,97) + preparació (8,27) + guillotinat (4,63) = **127,83 €**
    

---

## 10\. NOTES PER A FUTURES COMANDES

-   **Paper químic:** Els preus per full SRA3 (blanc 0,1154 €, blau 0,1390 €, groc 0,1027 €) són específics d'aquest producte i no es troben a `costosOperatius2026.md`; cal mantenir-los actualitzats en aquest document.
    
-   **Cost d'impressió:** S'usa `color_SRA3_base = 0,03966 €/cara` de `costosOperatius2026.md` per a color, i `b_n_SRA3_base = 0,00556 €/cara` ×8 per a B/N. Si canvia el fitxer de costos, actualitzar aquí.
    
-   **Guillotinat:** S'unifica amb el procediment de flyers v2.2 (preparació 5 min fix + 3 min/500 fulls, mínim 10 min, a 27,78 €/h).
    
-   **Preparació:** S'unifica amb el procediment de flyers v2.2 (15 min base a 33,08 €/h; 30 min amb numeració).
    
-   **Transport:** El cost de `transport_per_comanda = 5,00 €` no està inclòs en aquest càlcul; afegir-lo si s'aplica.
    
-   **Manteniment extern:** El cost de `manteniment_equip_extern = 2,00 €` per treball no està inclòs; valorar si s'ha d'afegir com a cost fix addicional.
    
-   **Marge:** Revisar el marge segons volum (secció 0) abans de tancar el preu de venda.
    
-   **Maculatura:** S'usa la maculatura estàndard de 4 unitats per model de `costosOperatius2026.md`; si s'afegeixen nous productes, revisar `[maculatura]`.
    

---

*Document guardat com a: `costosImpressioPaperTalonaris.md` — Versió 2.0*
