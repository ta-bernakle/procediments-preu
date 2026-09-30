# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A5 ENCOLATS AMB RÚSTICA FRESADA

**VERSIÓ:** 1.0  
**DATA:** 2026-09-30  
**TIPUS:** Enquadernació rústica fresada (externa)  
**Marge per defecte:** 50%  
**Gruix mínim del llom:** 4,5-5 mm

---

## 1. OBJECTIU

Càlcul de costos per a llibrets A5 amb enquadernació rústica fresada (llom fresat i encolat amb cola pur), impresos sobre SRA3, amb coberta i interior de gramatges i colors diferents.

Aquest procediment s'utilitza per a llibrets amb **gruix de llom igual o superior a 4,5-5 mm**. Per a gruixos inferiors, el grapat és més econòmic i adequat.

---

## 2. ESTRUCTURA FÍSICA DEL PRODUCTE

Un llibret A5 es compon de plecs (quaderns) de 4 pàgines A5, que s'imprimeixen a raó de 2 plecs per full SRA3 (un a cada cara).

- 1 full SRA3 = 2 plecs = 8 pàgines A5 (4 per cara)
- Cada plec = 4 pàgines A5 = ½ full SRA3

**Exemple per a 112 pàgines totals:**

| Component | Pàgines | Plecs (4 pàg.) | Fulls SRA3 per unitat |
|-----------|---------|----------------|------------------------|
| Coberta   | 4       | 1              | 0,5                    |
| Interior  | 108     | 27             | 13,5                   |
| **Total** | **112** | **28**         | **14,0**               |

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

### Enquadernació rústica fresada (costos externs)
- Fendir llom i cortesia = **0,38 €/llibre**
- Fresat i encolat fins a 1 cm gruix de llom = **0,69 €/llibre**
- Guillotinat a 3 cantos = **0,75 €/llibre**
- Posada en màquina = **12,00 €** (fix per comanda)
- **Total variable per llibre = 1,82 €**
- Si el gruix del llom supera 1 cm → consultar sobrecost

### Consum elèctric + manteniment
- Potència equip = 4,5 kW (només impressora i equip auxiliar)
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

### 4.5 Enquadernació rústica fresada
Cost_enquadernació = (Unitats_producció × 1,82) + 12,00 €

On:
- 1,82 € = 0,38 (fendir) + 0,69 (fresat/encolat) + 0,75 (guillotinat 3 cantos)
- 12,00 € = posada en màquina (fix)

### 4.6 Electricitat + manteniment
Cost_electricitat = (Fulls_SRA3_totals / 1440) × 4,5 × 0,15 €
Cost_manteniment = 2,00 €

*(Nota: no hi ha temps de plegat/grapat perquè l'enquadernació és externa.)*

### 4.7 Preparació (imposició)
Cost_preparació = 8,27 € + (Nombre_models - 1) × 8,27 €

### 4.8 Manipulat
Cost_manipulat = (Nombre_models × 5 / 60) × 19,93 €

### 4.9 Transport
Cost_transport = 5,00 €

### 4.10 Cost total i preu de venda
COST TOTAL PRODUCCIÓ = Cost_paper_total + Cost_impressió_total + Cost_enquadernació

Cost_electricitat + Cost_manteniment + Cost_preparació

Cost_manipulat + Cost_transport

PREU VENDA CLIENT = COST TOTAL PRODUCCIÓ × (1 + Marge)
PREU PER UNITAT = PREU VENDA CLIENT / Unitats_client

### 4.11 Temps d'impressió
Temps_impressió (minuts) = (Fulls_SRA3_totals / 1440) × 60

---

## 5. EXEMPLES VERIFICATS

### 5.1 Llibret 112 pàgines (coberta color 250 g + interior color 80 g òfset)

**Dades:** 50 unitats, 1 model, factor click 1,2, marge 50%

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 50 + 4 | 54 |
| Fulls interior | 54 × (108/8) | 729 |
| Fulls coberta | 54 × (4/8) | 27 |
| Total fulls SRA3 | 729 + 27 | 756 |
| Cost paper interior | 729 × (0,080×0,144×1,75) | 14,70 € |
| Cost paper coberta | 27 × 0,0684 | 1,85 € |
| Cost impressió (×1,2) | 756 × 2 × 0,059 × 1,2 | 107,05 € |
| Cost enquadernació | (54 × 1,82) + 12,00 | 110,28 € |
| Electricitat | (756/1440)×4,5×0,15 | 0,35 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **251,16 €** |
| **PREU VENDA (+50%)** | 251,16 × 1,50 | **376,74 €** |
| **PREU PER UNITAT** | 376,74 / 50 | **7,53 €** |

**Gruix llom:** 54 fulls interiors × 0,1 mm + 0,25 mm coberta ≈ 5,65 mm ✅

### 5.2 Llibret 140 pàgines (coberta color 250 g + interior color 80 g òfset)

**Dades:** 50 unitats, 1 model, factor click 1,2, marge 50%

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 50 + 4 | 54 |
| Fulls interior | 54 × (136/8) | 918 |
| Fulls coberta | 54 × (4/8) | 27 |
| Total fulls SRA3 | 918 + 27 | 945 |
| Cost paper interior | 918 × 0,02016 | 18,51 € |
| Cost paper coberta | 27 × 0,0684 | 1,85 € |
| Cost impressió (×1,2) | 945 × 2 × 0,059 × 1,2 | 133,81 € |
| Cost enquadernació | (54 × 1,82) + 12,00 | 110,28 € |
| Electricitat | (945/1440)×4,5×0,15 | 0,44 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **286,82 €** |
| **PREU VENDA (+50%)** | 286,82 × 1,50 | **430,23 €** |
| **PREU PER UNITAT** | 430,23 / 50 | **8,60 €** |

**Gruix llom:** 68 fulls interiors × 0,1 mm + 0,25 mm coberta ≈ 7,05 mm ✅

---

## 6. NOTES

1. Aquest procediment s'utilitza per a **gruixos de llom ≥ 4,5-5 mm**. Per a gruixos inferiors, usar el procediment de grapat.
2. El guillotinat a 3 cantos de l'enquadernador substitueix el guillotinat previ del procediment de grapat.
3. No hi ha plegat automàtic: els plecs els gestiona l'enquadernador.
4. La posada en màquina (12 €) és un cost fix per comanda.
5. Si el gruix del llom supera 1 cm, cal consultar sobrecost amb l'enquadernador.
6. El marge de benefici s'aplica al final sobre el cost total de producció.

---

## FI DEL PROCEDIMENT (VERSIÓ 1.0)
