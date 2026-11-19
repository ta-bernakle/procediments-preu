# 

# 📄 PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE DESPLEGABLES A5–A3+ (UN SOL FULL) A LA DIGITAL — v2.0

*(Alineat amb ProcedimentFlyersNegreOColor v2.2 i costosOperatius2026.md)*

---

> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

> 🔄 **CANVI v2.0:** S'elimina el **factor multiplicador de click** (×6, ×4, ×3). El cost d'impressió s'obté directament de `costosOperatius2026.md` (`color_SRA3_base = 0,03966 €/cara`). S'unifiquen guillotinat, preparació, empaquetat i transport amb el procediment de flyers v2.2. S'afegeix nota completa de marge comercial i secció de notes per a futures comandes. Es corregeix el preu de l'òfset 160 g (1,60 €/kg segons fitxer, no 1,75 €/kg).

---

## 1\. OBJECTIU

Càlcul de costos per a desplegables impresos en color sobre SRA3, en un sol full (no enquadernats), amb plegat industrial extern i sense grapes.

S'aplica a desplegables amb format final obert (desplegat) des de DIN A5 fins a DIN A3+ (màxim SRA3).

---

## 2\. NOMENCLATURA

Per evitar confusions, sempre s'ha d'especificar:

| Concepte | Definició | Exemple |
| --- | --- | --- |
| Mida oberta (desplegada) | Mida final del desplegable quan està completament desplegat | DIN A3 |
| Mida tancada (plegada) | Mida final del desplegable quan està plegat (format de lliurament) | DIN A4 |

---

## 3\. ESTRUCTURA FÍSICA DEL PRODUCTE

Un desplegable és un únic full SRA3, imprès a doble cara i plegat posteriorment.

**1 desplegable = 1 full SRA3 (2 cares impreses)**

| Mida oberta | Mida tancada | Fulls SRA3 per unitat |
| --- | --- | --- |
| DIN A3 | DIN A4 | 1 |
| DIN A4 | DIN A5 | 1 |
| DIN A5 | DIN A6 | 1 |

> 📌 **Nota:** No hi ha diferenciació entre interior i coberta, ja que és un sol full.

---

## 4\. DETERMINACIÓ DE DESPLEGABLES PER FULL SRA3

**Fórmula (mateixa nomenclatura que flyers v2.2):**

elements\_ample = part\_entera(zona\_útil\_ample / amplada\_element)
elements\_alt   = part\_entera(zona\_útil\_alt / altura\_element)
total\_per\_full = elements\_ample × elements\_alt

On zona útil SRA3 = **304 × 434 mm** (320×450 mm menys 8 mm de vora per costat).

| Mida oberta (desplegada) | Dimensions (cm) | Desplegables per SRA3 |
| --- | --- | --- |
| DIN A3 | 42,0 × 29,7 | 1 |
| DIN A4 | 29,7 × 21,0 | 2 |
| DIN A5 | 21,0 × 14,8 | 4 |
| 210 × 297 mm | 21,0 × 29,7 | 2 |

> 📌 **Nota:** En desplegables, cada unitat és **un sol full SRA3 sencer** (no es talla en peces individuals abans del plegat). La columna "Desplegables per SRA3" indica quantes unitats de mida oberta caben en un SRA3 **abans del plegat**, però el càlcul de fulls SRA3 per unitat és sempre **1 full per desplegable** (secció 6). La taula serveix per calcular la maculatura de plegadora (secció 5.2).

---

## 5\. MACULATURA (PROVES)

S'afegeix maculatura per a dos processos:

### 5.1. Maculatura d'impressora (ajust de color i mides)

Maculatura\_impressora = 5 fulls SRA3

### 5.2. Maculatura de plegadora (preparació de la màquina)

Base: **15 unitats en format final obert**

La conversió a fulls SRA3 depèn de quants desplegables caben per full:

Maculatura\_plegadora (SRA3) = SOSTRE(15 / Desplegables\_per\_SRA3)

| Mida oberta | Desplegables/SRA3 | Càlcul | Fulls SRA3 |
| --- | --- | --- | --- |
| DIN A3 | 1 | 15/1 = 15 | 15 |
| DIN A4 | 2 | 15/2 = 7,5 | 8 |
| DIN A5 | 4 | 15/4 = 3,75 | 4 |

### 5.3. Maculatura total

Maculatura\_total = Maculatura\_impressora + Maculatura\_plegadora

### 5.4. Unitats de producció

Unitats\_producció = Unitats\_client + Maculatura\_total

> ⚠️ **Nota:** La maculatura **NO es factura al client**, però **s'inclou al cost de producció** (el seu cost va dins del cost base).

---

## 6\. CÀLCUL DE FULLS SRA3

Fulls\_SRA3 = Unitats\_producció × 1

**Exemple:** 175 unitats, DIN A3 obert → 175 + 20 = 195 fulls SRA3.

> 📌 **Nota:** Cada desplegable és 1 full SRA3 sencer. No es divideix per elements/full perquè el desplegable ocupa tot el SRA3 (el plegat es fa després, sobre el full sencer).

---

## 7\. COST DE PAPER

### 7.1. Taula recomanada: cost directe per full SRA3 (preferent)

Usar la taula `[paper_full_sra3]` de `costosOperatius2026.md` quan el paper hi sigui tabulat:

Cost\_paper = Fulls\_SRA3 × Cost\_per\_full\_SRA3

### 7.2. Fórmula lineal (només per a papers no tabulats)

Cost\_paper = Fulls\_SRA3 × (Gramatge\_kg × 0,144 × Preu\_kg)

On:

-   `Gramatge_kg` \= gramatge en kg/m² (ex: 160 g = 0,160 kg)
    
-   `0,144` \= superfície d'un SRA3 (0,32 m × 0,45 m = 0,144 m²)
    
-   `Preu_kg` \= cost del paper per kg (segons proveïdor)
    

> ⚠️ **Atenció v2.0:** La fórmula lineal **no és fiable per a gramatges alts** (l'òfset 300 g real és 0,11406 €/full SRA3, molt lluny del que dona la fórmula amb 1,54 €/kg). Per a papers gruixuts o estucats, demanar preu real al proveïdor i usar la taula directa.

**Exemple (195 fulls, òfset 160 g a 1,60 €/kg segons fitxer):**

  

Cost\_paper = 195 × (0,160 × 0,144 × 1,60) = 195 × 0,03686 = 7,19 €

> ⚠️ **Correcció v2.0:** L'exemple original feia servir 1,75 €/kg per a òfset 160 g, però `costosOperatius2026.md` indica `ofset_160 = 1,60 €/kg`. **Corregit.**

---

## 8\. IMPRESSIÓ (DIGITAL, DOBLE CARA, COLOR)

### 8.1. Cost d'impressió (sense factor multiplicador) — ⚠️ CANVI v2.0

El cost d'impressió s'obté directament de `costosOperatius2026.md`, secció `[impressio]`. **No s'aplica cap factor de volum.** El preu per click ja és el cost real per cara impresa segons la màquina i el format.

| Concepte | Cost (€/cara) | Font |
| --- | --- | --- |
| B/N SRA3 | 0,00556 | `b_n_SRA3_base` |
| Color SRA3 | 0,03966 | `color_SRA3_base` |

**Fórmula:**

Cost\_impressió = Fulls\_SRA3 × 2 cares × 0,03966 €/cara

*(Sempre doble cara: 2 clicks per full SRA3)*

> ❌ **Eliminat v2.0:** Taula de factors multiplicadors (×6 fins a 250 clics, ×4 de 251 a 500, ×3 de 501 a 1.000). Ja no s'aplica cap multiplicador al click. El preu base anterior de 0,059 €/cara tampoc no coincidia amb `costosOperatius2026.md`; el valor correcte és **0,03966 €/cara**.

**Exemple (195 fulls):**

  

Cost\_impressió = 195 × 2 × 0,03966 = 15,47 €

*(Abans amb factor ×6 i 0,059 €: 138,06 €. **Diferència enorme:** \-122,59 €)*

---

## 9\. GUILLOTINAT PREVI AL PLECAT

S'unifica amb la taula de guillotina de flyers v2.2 (base 10 min, increment 3,96 min/1.000 fulls SRA3).

  

Temps\_guillotina (min) = 10 + (Fulls\_SRA3 − 1.000) / 1.000 × 3,96

Si `Fulls_SRA3` < 1.000 → temps base **10 min**.

  

Cost\_guillotinat = (Temps\_guillotina / 60) × 27,78 €

**Exemple (195 fulls):**

  

195 < 1.000 → temps base 10 min
Cost = (10/60) × 27,78 = 4,63 €

> 📌 **Coherència v2.0:** La fórmula pròpia anterior (`MÀXIM(10, 5 + CEILING(Fulls/500) × 3)`) s'ha substituït per la taula de flyers v2.2 per coherència entre procediments.

---

## 10\. PLECAT INDUSTRIAL (EXTERN)

S'utilitza plegadora industrial externa amb els següents paràmetres:

-   Preu/hora: **39,65 €** (`[ma_d_obra] plegat_grapat_extern`)
    
-   Preparació màquina: **15 minuts** (0,25 h)
    
-   Rendiment: **6.000 fulls/hora** (promig)
    

Temps\_prep\_plegat = 15 / 60 = 0,25 h
Temps\_prod\_plegat = Fulls\_SRA3 / 6000  (en hores)
Temps\_total\_plegat = Temps\_prep\_plegat + Temps\_prod\_plegat
Cost\_plegat = Temps\_total\_plegat × 39,65 €

**Exemple (195 fulls):**

  

Preparació: 0,25 h
Producció: 195/6000 = 0,0325 h
Total: 0,2825 h
Cost: 0,2825 × 39,65 = 11,20 €

---

## 11\. FENDIT (SI GRAMATGE > 170 g O PAPER ESTUCAT)

En cas de gramatges superiors a 170 g (especialment en papers estucats), cal afegir un fendit previ al plegat per evitar esquerdaments a les vores del plec.

**Paràmetres:**

-   Preu/hora: **31,70 €** (`[ma_d_obra] fendit`)
    
-   Preparació màquina: **10 minuts** (0,1667 h)
    
-   Rendiment variable segons llargada del full (en direcció d'alimentació):
    

| Llargada del full | Rendiment (peces/hora) |
| --- | --- |
| ≥ 42 cm (SRA3 apaïsat) | 1.200 |
| < 42 cm (SRA3 vertical o més petit) | 1.700 |

Si gramatge > 170 g O paper estucat = TRUE:
    Temps\_prep\_fendit = 10 / 60 = 0,1667 h
    Si llargada\_full >= 42 cm:
        Temps\_prod\_fendit = Fulls\_SRA3 / 1200
    Sinó:
        Temps\_prod\_fendit = Fulls\_SRA3 / 1700
    
    Temps\_total\_fendit = Temps\_prep\_fendit + Temps\_prod\_fendit
    Cost\_fendit = Temps\_total\_fendit × 31,70 €
Sinó:
    Cost\_fendit = 0 €

**Exemple (195 fulls, SRA3 vertical <42 cm, paper estucat 200 g):**

  

Preparació: 0,1667 h
Producció: 195/1700 = 0,1147 h
Total: 0,2814 h
Cost: 0,2814 × 31,70 = 8,92 €

---

## 12\. PREPARACIÓ / IMPOSICIÓ

S'unifica amb flyers v2.2: **15 min base + 5 min/model addicional** (33,08 €/h).

Cost\_preparació = 15/60 × 33,08 + (Nombre\_models − 1) × (5/60 × 33,08)
Cost\_preparació = 8,27 € + (Nombre\_models − 1) × 2,76 €

**Exemple (1 model):** 8,27 €

> ⚠️ **Correcció v2.0:** L'original feia servir 4 min/model addicional (2,21 €). S'unifica a **5 min/model** (2,76 €) per coherència amb flyers v2.2. El model addicional és el mateix concepte (document diferent que cal imposar).

---

## 13\. EMPAQUETAT / MANIPULAT

S'unifica amb flyers v2.2: **6 € base + 1,5 min/model** (19,93 €/h).

  

Cost\_manipulat = 6,00 € + (Nombre\_models × 1,5/60 × 19,93)
Cost\_manipulat = 6,00 € + Nombre\_models × 0,50 €

**Exemple (1 model):** 6,00 € + 0,50 € = **6,50 €**

> ⚠️ **Correcció v2.0:** L'original feia servir només `(models × 5/60) × 19,93` \= 1,66 €/model, sense base de 6 €. S'unifica amb flyers v2.2 (6 € base + 1,5 min/model). **Diferència:** 1,66 € → 6,50 €.

---

## 14\. TRANSPORT

S'unifica amb flyers v2.2: **6,00 €** (base) + `[operatius] transport_per_comanda`.

Cost\_transport = 6,00 €

> ⚠️ **Correcció v2.0:** L'original feia servir 5,00 € (`transport_per_comanda`). S'unifica a **6,00 €** per coherència amb flyers v2.2 (que inclou base + transport). Si es vol mantenir 5,00 €, cal documentar per què difereix.

---

## 15\. MARGE COMERCIAL

  

Cost\_total\_producció = Cost\_paper + Cost\_impressió + Cost\_guillotinat + Cost\_plegat + Cost\_fendit + Cost\_preparació + Cost\_manipulat + Cost\_transport
Preu\_venda\_client = Cost\_total\_producció × (1 + Marge)
Preu\_per\_unitat = Preu\_venda\_client / Unitats\_client

**Marge recomanat segons volum** (vegeu nota inicial):

-   Comandes petites: **100–150%**
    
-   Comandes mitjanes: **75–100%**
    
-   Comandes grans: **50–75%**
    
-   Comandes molt grans: **25–50%**
    

> ⚠️ **Nota v2.0:** El marge per defecte del 50% de l'original és **insuficient** per a comandes petites (la majoria de desplegables són tirades curtes). Cal ajustar el marge segons el volum i el client. Per a un client recurrent, es pot aplicar un marge fix pactat (p. ex. 100–130%) sempre que cobreixi costos indirectes.

---

## 16\. TEMPS D'IMPRESSIÓ (ESTIMAT — ORIENTATIU)

Temps\_impressió (minuts) = (Fulls\_SRA3 / 1440) × 60

**Exemple (195 fulls):** (195/1440)×60 = 8,13 minuts

> ⚠️ **Nota v2.0:** Aquest càlcul assumeix 1.440 fulls/hora (24 fulls/minut). **És una estimació orientativa**, no un cost. No s'usa a l'estructura de costos (secció 15). Si es vol usar per planificació, confirmar el rendiment real de la Xerox Versant 4100 Pro.

---

## 17\. EXEMPLE VERIFICAT (ESTÀNDARD) — v2.0

### Dades d'entrada

| Paràmetre | Valor |
| --- | --- |
| Producte | Díptic DIN A3 obert / A4 tancat |
| Unitats | 175 |
| Models | 1 |
| Paper | Òfset blanc 160 g |
| Preu paper | **1,60 €/kg** (corregit v2.0) |
| Impressió | Color, doble cara |
| Plegat | Díptic simple (1 plec) |
| Fendit | NO (160 g < 170 g, no estucat) |
| Maculatura impressora | 5 fulls SRA3 |
| Maculatura plegadora | 15 fulls SRA3 (DIN A3 = 1/SRA3) |
| Marge | **100%** (comanda petita, client recurrent) |

### Càlculs

| Concepte | Fórmula | Resultat |
| --- | --- | --- |
| Maculatura total | 5 + 15 | 20 fulls |
| Unitats producció | 175 + 20 | 195 |
| Fulls SRA3 | 195 × 1 | 195 |
| Cost paper | 195 × (0,160×0,144×1,60) | **7,19 €** |
| Cost impressió | 195 × 2 × 0,03966 | **15,47 €** |
| Cost guillotinat | (10/60) × 27,78 | **4,63 €** |
| Cost plegat | (0,25 + 195/6000) × 39,65 | **11,20 €** |
| Cost fendit | No aplica | **0,00 €** |
| Preparació | 15/60 × 33,08 | **8,27 €** |
| Manipulat | 6,00 + 1×0,50 | **6,50 €** |
| Transport | fix | **6,00 €** |
| **TOTAL PRODUCCIÓ** |  | **59,26 €** |
| Marge 100% | 59,26 × 2,00 | **118,52 €** |
| **Preu per unitat** | 118,52 / 175 | **0,677 €** |

> ⚠️ **Comparació amb l'original:** El cost de producció passa de **176,68 € a 59,26 €** (-117,42 €). El motiu principal és l'eliminació del factor ×6 al click (138,06 € → 15,47 €). El preu de venda amb marge 100% és **118,52 €** (0,68 €/unitat), en lloc de 265,02 € (1,51 €/unitat) amb marge 50%. **El marge s'ha apujat a 100% perquè el cost base és molt més baix i cal cobrir costos indirectes.**

---

## 18\. EXEMPLE AMB FENDIT (NOU v2.0)

### Dades d'entrada

| Paràmetre | Valor |
| --- | --- |
| Producte | Tríptic DIN A4 obert / A5 tancat |
| Unitats | 300 |
| Models | 1 |
| Paper | Estucat 200 g |
| Preu paper | **0,11406 €/full SRA3** (preu real proveïdor, taula directa) |
| Impressió | Color, doble cara |
| Plegat | Tríptic (2 plecs) |
| Fendit | **SÍ** (estucat, >170 g) |
| Maculatura impressora | 5 fulls SRA3 |
| Maculatura plegadora | 8 fulls SRA3 (DIN A4 = 2/SRA3 → 15/2 = 8) |
| Marge | **100%** (comanda petita-mitjana) |

### Càlculs

| Concepte | Fórmula | Resultat |
| --- | --- | --- |
| Maculatura total | 5 + 8 | 13 fulls |
| Unitats producció | 300 + 13 | 313 |
| Fulls SRA3 | 313 × 1 | 313 |
| Cost paper | 313 × 0,11406 | **35,70 €** |
| Cost impressió | 313 × 2 × 0,03966 | **24,83 €** |
| Cost guillotinat | (10/60) × 27,78 | **4,63 €** |
| Cost plegat | (0,25 + 313/6000) × 39,65 | **11,98 €** |
| Cost fendit | (0,1667 + 313/1700) × 31,70 | **11,12 €** |
| Preparació | 15/60 × 33,08 | **8,27 €** |
| Manipulat | 6,00 + 1×0,50 | **6,50 €** |
| Transport | fix | **6,00 €** |
| **TOTAL PRODUCCIÓ** |  | **109,03 €** |
| Marge 100% | 109,03 × 2,00 | **218,06 €** |
| **Preu per unitat** | 218,06 / 300 | **0,727 €** |

> ✅ **Aquest exemple valida la fórmula de fendit** (secció 11) amb paper estucat >170 g. El fendit afegeix **11,12 €** al cost base.

---

## 19\. NOTES PER A FUTURES COMANDES

-   **Impressió: usar directament `color_SRA3_base = 0,03966 €/cara` de `costosOperatius2026.md`. No aplicar cap factor multiplicador.**
    
-   Sempre doble cara: `Cost_impressió = Fulls_SRA3 × 2 × 0,03966 €`.
    
-   **1 desplegable = 1 full SRA3** (no es divideix per elements/full).
    
-   **Maculatura:** 5 fulls impressora + `SOSTRE(15 / Desplegables_per_SRA3)` de plegadora. **No es factura al client**, però s'inclou al cost.
    
-   **Paper:** usar taula directa `[paper_full_sra3]` si existeix; si no, fórmula lineal €/kg amb nota que pot fallar en gramatges alts.
    
-   **Guillotinat:** taula flyers v2.2 (base 10 min, increment 3,96 min/1.000 fulls SRA3).
    
-   **Fendit:** només si gramatge >170 g o paper estucat. Rendiment 1.200 peces/h (≥42 cm) o 1.700 peces/h (<42 cm).
    
-   **Preparació:** 15 min base + 5 min/model (8,27 € + 2,76 €/model).
    
-   **Manipulat:** 6 € base + 1,5 min/model (6,00 € + 0,50 €/model).
    
-   **Transport:** 6,00 € fix.
    
-   **Marge:** ajustar segons volum i client. Per a comandes petites, 100–150%. El 50% per defecte és insuficient.
    
-   **Temps d'impressió:** orientatiu, no s'usa a l'estructura de costos.
    
-   Guardar aquest document com a referència per a futures consultes.
    

---

## 20\. TAULA DE MACULATURA DE PLECADORA (REFERÈNCIA RÀPIDA)

| Desplegables per SRA3 | Càlcul | Fulls SRA3 (arrodonit) |
| --- | --- | --- |
| 1 (DIN A3) | 15 / 1 = 15 | 15 |
| 2 (DIN A4) | 15 / 2 = 7,5 | 8 |
| 3 | 15 / 3 = 5 | 5 |
| 4 (DIN A5) | 15 / 4 = 3,75 | 4 |
| 6 | 15 / 6 = 2,5 | 3 |
| 8 | 15 / 8 = 1,875 | 2 |
| 9+ | 15 / n < 2 | 2 (mínim 2 per ajustos) |

---

## 21\. OBSERVACIONS FINALS

-   Sense grapes (no s'aplica cost de grapes ni grapat manual).
    
-   Un sol tipus de paper per treball (no hi ha coberta/interior diferenciats).
    
-   El fendit només s'aplica si el gramatge supera 170 g o el paper és estucat.
    
-   La llargada del full per al càlcul del fendit es refereix a la direcció d'alimentació de la plegadora.
    
-   **El factor multiplicador del click s'ha eliminat.** El cost d'impressió és directe de `costosOperatius2026.md`.
    
-   La maculatura NO es factura al client, però s'inclou al cost de producció.
    
-   **Procediment alineat amb `ProcedimentFlyersNegreOColor v2.2`** en guillotinat, preparació, empaquetat, transport i marge.
    

---

📌 **Versió:** 2.0  
📅 **Data:** 2026-11-19  
✏️ **Canvis v2.0:** Eliminat factor multiplicador de click (×6, ×4, ×3); corregit preu click a 0,03966 €/cara; corregit preu òfset 160 g a 1,60 €/kg; unificat guillotinat, preparació, empaquetat i transport amb flyers v2.2; afegida nota completa de marge comercial; afegida secció de notes per a futures comandes; afegit exemple amb fendit (estucat 200 g); actualitzada nomenclatura d'elements/full; explicitada maculatura no facturada; marcat temps d'impressió com a orientatiu.  
🔄 **Pendent:** validar marges comercials sense factor de click amb casos històrics. Confirmar rendiment real de la Xerox Versant 4100 Pro (1.440 fulls/h) si es vol usar per planificació.

---

**FI DEL PROCEDIMENT**  
*Guardat com a `ProcedimentDesplegablesA5-A3+ v2.0.md`*
