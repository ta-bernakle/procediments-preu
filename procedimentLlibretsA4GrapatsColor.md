# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A4 GRAPATS A COLOR (SRA3)

**VERSIÓ:** 1.0  
**DATA:** 2026-11-25  
**TIPUS:** Impressió color SRA3 + plegat i grapat (mida final A4 tancat)  
**Marge per defecte:** escalat (50% - 200%)  
**Basat en:** `procedimentLlibretsA5GrapatsColor.md` v5.0 i `costosOperatius2026.md` v1.0

---

> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

---

## 1\. OBJECTIU

Càlcul de costos per a **llibrets A4 grapats** (mida final A4 tancat), impresos **en color sobre SRA3**, amb plegat, grapat i retallat.

Aquest procediment és per a **color sobre SRA3 amb mida final A4**. Per a **A5 sobre SRA3**, usar `procedimentLlibretsA5GrapatsColor.md`. Per a **blanc i negre sobre A4 en línia**, usar `procedimentLlibretsA5GrapatsBNEnLinia.md`.

---

## 2\. ESTRUCTURA FÍSICA DEL PRODUCTE

-   **1 full SRA3 = 1 plec sencer de la revista** (4 pàgines A4: 2 per cara)
    
-   Cada plec = **4 pàgines A4** \= ½ full SRA3 per cara → **1 full SRA3 per plec**
    
-   Un llibret A4 de N pàgines necessita **N/4 fulls SRA3** (arrodonit a l'enter superior, ja que les pàgines han de ser múltiple de 4)
    

**Exemple per a 24 pàgines totals:**

| Component | Pàgines | Plecs (4 pàg.) | Fulls SRA3 per unitat |
| --- | --- | --- | --- |
| Coberta | 4 | 1 | 1,0 |
| Interior | 20 | 5 | 5,0 |
| **Total** | **24** | **6** | **6,0** |

> **Nota:** a diferència de l'A5 (on 1 SRA3 = 2 plecs = 8 pàg. A5), en A4 **1 SRA3 = 1 plec = 4 pàg. A4**. Per tant, el nombre de fulls SRA3 per unitat és el **nombre de plecs**, no la meitat.

---

## 3\. PARÀMETRES FIXOS

### Impressió SRA3

-   Cost per click color SRA3 = **0,03966 €/cara** (font: `costosOperatius2026.md`)
    
-   Velocitat impressora = 24 fulls SRA3/min (1.440 fulls/hora)
    
-   Factor de click per defecte = **1,0** (ajustable segons volum)
    

### Paper

-   Superfície SRA3 = 0,144 m²
    
-   Cost paper estucat 135 g = **1,75 €/kg** (interior)
    
-   Cost paper estucat 250 g = **1,90 €/kg** (coberta)
    
-   Cobertes per full SRA3 = 1 (cada SRA3 de coberta dona 1 plec de coberta = 4 pàg. A4)
    

### Preparació documents (imposició)

-   Temps base per feina = 15 minuts
    
-   Cost preparació base = **8,27 €** (15 min × 33,08 €/h)
    
-   Per cada model addicional = +5 minuts (+2,76 €)
    
-   Cost hora = 33,08 €/hora
    

### Guillotinat previ

-   Preparació fixa = 5 minuts
    
-   Processament = 3 minuts / 500 fulls SRA3
    
-   Temps mínim = 10 minuts
    
-   Cost hora = 27,78 €/hora
    
-   (Font: `costosOperatius2026.md`, secció `[temps_estandar]` i `[ma_d_obra]`)
    

### Plegat, grapat i retallat

-   Preparació base (4 pàgines A4) = 15 minuts
    
-   Increment = +3 minuts / cada 4 pàgines addicionals
    
-   Límit automàtic de grapat = **64 pàgines A4** (equivalent a 32 pàg. A5; la màquina té la mateixa capacitat teòrica)
    
-   Velocitat de producció = **850 revistes/hora** (promig 800-900 revistes/hora a l'alçadora-grapadora; el sistema de cadena és solidari amb la velocitat de plegat/grapat/retallat, i és el mateix temps per exemplar en A4 que en A5)
    
-   Cost hora = 39,65 €/hora
    
-   Cost grapa (amortitzada) = **0,0065333 €**
    
-   Grapes per manual = 2
    

### Consum elèctric + manteniment

-   Potència equip = 4,5 kW
    
-   Preu electricitat = 0,15 €/kWh
    
-   Manteniment per treball = 2,00 €
    

### Manipulat / empaquetat

-   Temps per model = 5 minuts
    
-   Cost hora = 19,93 €/hora
    

### Transport

-   Cost per comanda (entrega única) = 5,00 €
    

### Maculatura

-   **Unitats addicionals per prova = 2 o 3 llibrets sencers per model** (a criteri de l'operari; per defecte **3 llibrets sencers** per poder fer proves i ajustos interns)
    
-   S'aplica per separat a interior i coberta, però com que cada llibret sencer inclou coberta + interior, es tradueix en:
    
    -   Fulls SRA3 de coberta addicionals = `Maculatura_llibrets × (Pàgines_coberta / 4)`
        
    -   Fulls SRA3 d'interior addicionals = `Maculatura_llibrets × (Pàgines_interior / 4)`
        
-   **NO es factura al client**
    

### Marge de benefici

-   Escalat segons volum i tipus de client (veure apartat 6)
    

---

## 4\. FÓRMULES

### 4.1 Maculatura

Maculatura\_llibrets = 3   (per defecte; pot ser 2 o 3 segons criteri)
Unitats\_producció = Unitats\_client + Maculatura\_llibrets

> **Nota:** a diferència de l'A5 (on la maculatura eren 4 unitats soltes per model), aquí la maculatura són **llibrets sencers** (coberta + interior), perquè cal fer proves i ajustos interns amb el producte complet.

### 4.2 Fulls SRA3 (per tipus de paper)

Fulls\_SRA3\_tipus = Unitats\_producció × (Pàgines\_tipus / 4)
Fulls\_SRA3\_totals = Fulls\_SRA3\_interior + Fulls\_SRA3\_coberta

> **Nota:** el divisor és **4** (pàgines A4 per full SRA3), no 8 com en A5.

### 4.3 Cost paper

Cost\_paper\_tipus = Fulls\_SRA3\_tipus × (Gramatge\_kg × 0,144 × Preu\_kg\_tipus)
Cost\_paper\_total = Cost\_paper\_interior + Cost\_paper\_coberta

### 4.4 Cost impressió

Cost\_impressió = Fulls\_SRA3\_totals × 2 × 0,03966 € × Factor\_click

### 4.5 Guillotinat previ

Temps\_guillotinat (min) = MÀXIM(10, 5 + CEILING(Fulls\_SRA3\_totals / 500) × 3)
Cost\_guillotinat = (Temps\_guillotinat / 60) × 27,78 €

### 4.6 Plegat, grapat i retallat

Si Pàgines\_A4 ≤ 64:
    Temps\_prep\_plegat (min) = 15 + ((Pàgines\_A4 - 4) / 4) × 3
    Temps\_prod\_plegat (h) = Unitats\_producció / 850
    Temps\_total\_plegat (h) = (Temps\_prep\_plegat / 60) + Temps\_prod\_plegat
    Cost\_plegat/grapat = Temps\_total\_plegat × 39,65 €
Si Pàgines\_A4 > 64:
    → PREGUNTAR a l'usuari com gestionar els plecs addicionals

> **Nota:** la base de preparació és 4 pàgines A4 (1 plec = 1 SRA3), i l'increment és +3 min per cada 4 pàgines addicionals. El límit de 64 pàg. A4 equival al límit de 32 pàg. A5 de la mateixa alçadora-grapadora.

### 4.7 Grapes

Cost\_grapes = Unitats\_producció × 2 × 0,0065333 €

### 4.8 Electricitat + manteniment

Cost\_electricitat = Temps\_total\_plegat × 4,5 × 0,15 €
Cost\_manteniment = 2,00 €

### 4.9 Preparació (imposició)

Cost\_preparació = 8,27 € + (Nombre\_models - 1) × 2,76 €

### 4.10 Manipulat

Cost\_manipulat = (Nombre\_models × 5 / 60) × 19,93 €

### 4.11 Transport

Cost\_transport = 5,00 €

### 4.12 Cost total i preu de venda

COST TOTAL PRODUCCIÓ = Cost\_paper\_total + Cost\_impressió + Cost\_guillotinat
                     + Cost\_plegat/grapat + Cost\_grapes + Cost\_electricitat
                     + Cost\_manteniment + Cost\_preparació + Cost\_manipulat
                     + Cost\_transport
PREU VENDA CLIENT = COST TOTAL PRODUCCIÓ × (1 + Marge)
PREU PER UNITAT = PREU VENDA CLIENT / Unitats\_client

### 4.13 Temps d'impressió

Temps\_impressió (minuts) = (Fulls\_SRA3\_totals / 1440) × 60

---

## 5\. EXEMPLE VERIFICAT (400 unitats, 24 pàgines A4, 1 model, factor 1,0, maculatura 3 llibrets)

**Dades:**

-   Unitats\_client = 400
    
-   Pàgines coberta = 4 (250 g)
    
-   Pàgines interior = 20 (135 g)
    
-   Nombre\_models = 1
    
-   Factor\_click = 1,0
    
-   Maculatura\_llibrets = 3
    

**Càlculs:**

| Concepte | Fórmula | Resultat |
| --- | --- | --- |
| Unitats producció | 400 + 3 | 403 |
| Fulls interior | 403 × (20/4) | 2.015 |
| Fulls coberta | 403 × (4/4) | 403 |
| Total fulls SRA3 | 2.015 + 403 | 2.418 |
| Cost paper interior | 2.015 × (0,135 × 0,144 × 1,75) | 68,55 € |
| Cost paper coberta | 403 × (0,250 × 0,144 × 1,90) | 27,58 € |
| Cost impressió | 2.418 × 2 × 0,03966 | 191,80 € |
| Cost guillotinat | (20/60) × 27,78 | 9,26 € |
| Cost plegat/grapat | 0,624 × 39,65 | 24,74 € |
| Cost grapes | 403 × 2 × 0,0065333 | 5,27 € |
| Electricitat | 0,624 × 4,5 × 0,15 | 0,42 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** |  | **344,55 €** |
| **COST PER UNITAT** | 344,55 / 400 | **0,861 €** |

**Detall del plegat/grapat:**

-   Temps\_prep\_plegat = 15 + ((24 − 4)/4) × 3 = 15 + 15 = **30 min**
    
-   Temps\_prod\_plegat = 403 / 850 = **0,474 h**
    
-   Temps\_total\_plegat = 0,5 + 0,474 = **0,974 h** → Cost = 0,974 × 39,65 = **38,62 €**
    

> ⚠️ **Correcció respecte al càlcul de la taula:** el cost de plegat/grapat és **38,62 €** (no 24,74 €), perquè el temps de preparació és 30 min (0,5 h) i la producció és 0,474 h. Recalculem el total:

| Concepte | Resultat |
| --- | --- |
| Cost paper interior | 68,55 € |
| Cost paper coberta | 27,58 € |
| Cost impressió | 191,80 € |
| Cost guillotinat | 9,26 € |
| Cost plegat/grapat | 38,62 € |
| Cost grapes | 5,27 € |
| Electricitat | 0,66 € (0,974 × 4,5 × 0,15) |
| Manteniment | 2,00 € |
| Preparació | 8,27 € |
| Manipulat | 1,66 € |
| Transport | 5,00 € |
| **COST TOTAL** | **358,67 €** |
| **COST PER UNITAT** | **0,897 €** |

**Temps d'impressió:**  
(2.418 / 1440) × 60 = **100,75 minuts ≈ 101 minuts**

---

## 6\. PROPOSTA DE MARGE ESCALAT

| Escenari | Marge | Preu total | Preu/unitat | Comentari |
| --- | --- | --- | --- | --- |
| **Cost pur** | 0% | 358,67 € | 0,897 € | Referència interna |
| **Marge mínim** (volum, client fidel) | 40% | 502,14 € | 1,255 € | Competitiu |
| **Marge estàndard** (client habitual) | 50% | 538,01 € | 1,345 € | Referència |
| **Marge recomanat** (comanda petita) | 75% | 627,67 € | 1,569 € | Cobreix costos comercials |
| **Marge premium** (urgència) | 100% | 717,34 € | 1,793 € | Comandes especials |
| **Marge alt** (client nou) | 150% | 896,68 € | 2,242 € | Màxim recomanat |

---

## 7\. NOTES

1.  Aquest procediment és **exclusiu per a color sobre SRA3 amb mida final A4**.
    
2.  Per a **A5 sobre SRA3**, usar `procedimentLlibretsA5GrapatsColor.md`.
    
3.  Per a **blanc i negre sobre A4 en línia**, usar `procedimentLlibretsA5GrapatsBNEnLinia.md`.
    
4.  Per a **enquadernació rústica fresada**, usar `procedimentLlibretsA5RusticaFresada.md`.
    
5.  El cost de click color SRA3 (0,03966 €/cara) és el valor real del fitxer `costosOperatius2026.md`.
    
6.  La preparació base és de 15 minuts (8,27 €); cada model addicional suma 5 minuts (2,76 €).
    
7.  El guillotinat previ s'aplica al total de fulls SRA3 (interior + coberta).
    
8.  El plegat/grapat es calcula sobre el total de pàgines A4 del producte, amb base 4 pàg. i increment de 3 min per cada 4 pàg. addicionals.
    
9.  **La maculatura és de 2 o 3 llibrets sencers per model** (per defecte 3), per poder fer proves i ajustos interns. S'aplica per separat a interior i coberta, però com que cada llibret sencer inclou totes dues parts, el càlcul és `Maculatura_llibrets × (Pàgines_tipus / 4)` fulls SRA3 per tipus.
    
10.  **La velocitat de plegat/grapat/retallat és de 850 revistes/hora** (promig 800-900), perquè el sistema de cadena és solidari amb la velocitat de la cadena i el temps per exemplar és el mateix en A4 que en A5. El límit de grapat és de 64 pàg. A4 (equivalent a 32 pàg. A5).
     
11.  Si el producte supera les 64 pàgines A4, cal consultar com gestionar els plecs addicionals.
     
12.  El marge s'aplica al final sobre el cost total de producció.
     

---

## FI DEL PROCEDIMENT (VERSIÓ 1.0)
