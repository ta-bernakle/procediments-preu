# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A5 GRAPATS A COLOR

**VERSIÓ:** 4.0  
**DATA:** 2026-09-30  
**TIPUS:** Plegat automàtic + grapat  
**Marge per defecte:** 50%

---

## 1. OBJECTIU

Càlcul de costos per a llibrets A5 grapats, impresos sobre SRA3, amb coberta i interior de gramatges i colors diferents (color o blanc i negre).

---

## 2. ESTRUCTURA FÍSICA DEL PRODUCTE

Un llibret A5 es compon de plecs (quaderns) de 4 pàgines A5, que s'imprimeixen a raó de 2 plecs per full SRA3 (un a cada cara).

- 1 full SRA3 = 2 plecs = 8 pàgines A5 (4 per cara)
- Cada plec = 4 pàgines A5 = ½ full SRA3

**Exemple per a 24 pàgines totals:**

| Component | Pàgines | Plecs (4 pàg.) | Fulls SRA3 per unitat |
|-----------|---------|----------------|------------------------|
| Coberta   | 4       | 1              | 0,5                    |
| Interior  | 20      | 5              | 2,5                    |
| **Total** | **24**  | **6**          | **3,0**                |

---

## 3. PARÀMETRES FIXOS

### Impressió SRA3
- Cost per click color SRA3 = **0,059 €/cara**
- Cost per click blanc i negre SRA3 = **0,012 €/cara**
- Velocitat impressora = 24 fulls SRA3/min (1.440 fulls/hora)
- Factor de click per defecte = **1,2** (ajustable segons volum)

### Paper
- Superfície SRA3 = 0,144 m²
- Cost paper interior (90-170 g) = 1,75 €/kg
- Cost paper coberta (200-350 g) = 1,90 €/kg
- Cobertes per full SRA3 = 2

### Preparació documents (imposició)
- Temps base per feina = 15 minuts
- Cost preparació base = 8,27 €
- Per cada model addicional = +15 minuts (+8,27 €)
- Cost hora = 33,08 €/hora

### Guillotinat previ
- Preparació fixa = 5 minuts
- Processament = 3 minuts / 500 fulls SRA3
- Temps mínim = 10 minuts
- Cost hora = 27,78 €/hora

### Plegat i grapat automàtic
- Preparació base (8 pàgines) = 15 minuts
- Increment = +3 minuts / cada 4 pàgines addicionals
- Límit automàtic = 32 pàgines A5
- Velocitat producció = 1.000 revistes/hora
- Cost hora = 39,65 €/hora
- Cost grapa = 0,004 €
- Grapes per manual = 2

### Consum elèctric + manteniment
- Potència equip = 4,5 kW
- Preu electricitat = 0,15 €/kWh
- Manteniment per treball = 2,00 €

### Manipulat / empaquetat
- Temps per model = 5 minuts
- Cost hora = 19,93 €/hora

### Transport
- Cost per comanda (entrega única) = 5,00 €

### Maculatura
- Unitats addicionals per prova = 4 unitats per model (2 fulls SRA3 per model)
- S'aplica per separat a interior i coberta
- NO es factura al client

### Marge de benefici
- Marge per defecte = **50%**

---

## 4. FÓRMULES

### 4.1 Maculatura

Unitats_producció = Unitats_client + (Nombre_models × 4)

### 4.2 Fulls SRA3 (per tipus de paper)

Fulls_SRA3_tipus = Unitats_producció × (Pàgines_tipus / 8)
Fulls_SRA3_totals = Fulls_SRA3_interior + Fulls_SRA3_coberta


### 4.3 Cost paper

Cost_paper_tipus = Fulls_SRA3_tipus × (Gramatge_kg × 0,144 × Preu_kg_tipus)
Cost_paper_total = Cost_paper_interior + Cost_paper_coberta

### 4.4 Cost impressió

Cost_impressió_interior = Fulls_SRA3_interior × 2 × Cost_click × Factor_click
Cost_impressió_coberta = Fulls_SRA3_coberta × 2 × Cost_click × Factor_click
Cost_impressió_total = Cost_impressió_interior + Cost_impressió_coberta
On `Cost_click` = 0,059 € (color) o 0,012 € (B/N) segons correspongui.

### 4.5 Guillotinat previ

Temps_guillotinat (min) = MÀXIM(10, 5 + CEILING(Fulls_SRA3_totals / 500) × 3)
Cost_guillotinat = (Temps_guillotinat / 60) × 27,78 €

### 4.6 Plegat i grapat

Si Pàgines_A5 ≤ 32:
Temps_prep_plegat (min) = 15 + ((Pàgines_A5 - 8) / 4) × 3
Temps_prod_plegat (h) = Unitats_producció / 1000
Temps_total_plegat (h) = (Temps_prep_plegat / 60) + Temps_prod_plegat
Cost_plegat/grapat = Temps_total_plegat × 39,65 €
Si Pàgines_A5 > 32:
→ PREGUNTAR a l'usuari com gestionar els plecs addicionals

### 4.7 Grapes

Cost_grapes = Unitats_producció × 2 × 0,004 €


### 4.8 Electricitat + manteniment

Cost_electricitat = Temps_total_plegat × 4,5 × 0,15 €
Cost_manteniment = 2,00 €


### 4.9 Preparació (imposició)

Cost_preparació = 8,27 € + (Nombre_models - 1) × 8,27 €

### 4.10 Manipulat

Cost_manipulat = (Nombre_models × 5 / 60) × 19,93 €

### 4.11 Transport

Cost_transport = 5,00 €

### 4.12 Cost total i preu de venda

COST TOTAL PRODUCCIÓ = Cost_paper_total + Cost_impressió_total + Cost_guillotinat

Cost_plegat/grapat + Cost_grapes + Cost_electricitat

Cost_manteniment + Cost_preparació + Cost_manipulat

Cost_transport

PREU VENDA CLIENT = COST TOTAL PRODUCCIÓ × (1 + Marge)
PREU PER UNITAT = PREU VENDA CLIENT / Unitats_client

### 4.13 Temps d'impressió

Temps_impressió (minuts) = (Fulls_SRA3_totals / 1440) × 60

---

## 5. EXEMPLE VERIFICAT

### 5.1 Llibret 24 pàgines (coberta color 250 g + interior color 135 g)

**Dades:** 400 unitats, 1 model, factor click 1,2, marge 50%

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 400 + 4 | 404 |
| Fulls interior | 404 × (20/8) | 1.010 |
| Fulls coberta | 404 × (4/8) | 202 |
| Total fulls SRA3 | 1.010 + 202 | 1.212 |
| Cost paper interior | 1.010 × 0,03402 | 34,36 € |
| Cost paper coberta | 202 × 0,0684 | 13,82 € |
| Cost impressió (color ×1,2) | 1.212 × 2 × 0,059 × 1,2 | 171,62 € |
| Cost guillotinat | (14/60) × 27,78 | 6,48 € |
| Cost plegat/grapat | 0,854 × 39,65 | 33,86 € |
| Cost grapes | 404 × 2 × 0,004 | 3,23 € |
| Electricitat | 0,854 × 4,5 × 0,15 | 0,58 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **280,88 €** |
| **PREU VENDA (+50%)** | 280,88 × 1,50 | **421,32 €** |
| **PREU PER UNITAT** | 421,32 / 400 | **1,05 €** |

### 5.2 Llibret 16 pàgines (coberta color 250 g + interior B/N 80 g)

**Dades:** 50, 100 i 500 unitats, 1 model, factor click 1,2, marge 50%

| Concepte | 50 unitats | 100 unitats | 500 unitats |
|----------|-----------|-------------|-------------|
| Unitats producció | 54 | 104 | 504 |
| Fulls interior (B/N) | 81 | 156 | 756 |
| Fulls coberta (color) | 27 | 52 | 252 |
| Fulls SRA3 totals | 108 | 208 | 1.008 |
| Cost paper interior | 1,63 € | 3,14 € | 15,24 € |
| Cost paper coberta | 1,85 € | 3,56 € | 17,24 € |
| Cost impressió interior (B/N) | 2,33 € | 4,49 € | 21,77 € |
| Cost impressió coberta (color) | 3,82 € | 7,36 € | 35,68 € |
| Cost plegat/grapat | 16,02 € | 17,99 € | 33,85 € |
| Cost grapes | 0,43 € | 0,83 € | 4,03 € |
| Electricitat | 0,25 € | 0,28 € | 0,53 € |
| Manteniment | 2,00 € | 2,00 € | 2,00 € |
| Preparació | 8,27 € | 8,27 € | 8,27 € |
| Manipulat | 1,66 € | 1,66 € | 1,66 € |
| Transport | 5,00 € | 5,00 € | 5,00 € |
| **COST TOTAL** | **43,26 €** | **54,58 €** | **145,27 €** |
| **PREU VENDA (+50%)** | **64,89 €** | **81,87 €** | **217,91 €** |
| **PREU PER UNITAT** | **1,30 €** | **0,82 €** | **0,44 €** |

---

## 6. NOTES

1. El cost de click B/N (0,012 €/cara) és un valor de referència. Ajustar segons proveïdor.
2. El guillotinat previ s'aplica al total de fulls SRA3 (interior + coberta).
3. El plegat/grapat es calcula sobre el total de pàgines A5 del producte.
4. Si el producte supera les 32 pàgines, cal consultar com gestionar els plecs addicionals.
5. El marge de benefici s'aplica al final sobre el cost total de producció.

---

## FI DEL PROCEDIMENT (VERSIÓ 4.0)
