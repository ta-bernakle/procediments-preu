> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.


📄 PROCEDIMENT: LLIBRETS A5 ENCOLATS AMB RÚSTICA FRESADA
Fitxer: procedimentLlibretsA5RusticaFresada.md

markdown
# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A5 ENCOLATS AMB RÚSTICA FRESADA

**VERSIÓ:** 1.1  
**DATA:** 2026-11-16  
**TIPUS:** Enquadernació rústica fresada (externa)  
**Marge per defecte:** escalat (50% - 150%)  
**Gruix mínim del llom:** 4,5-5 mm  
**Substitueix:** Versió 1.0 (actualització de costos reals)

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
- Cost per click color SRA3 = **0,03966 €/cara**
- Cost per click blanc i negre SRA3 = **0,00556 €/cara**
- Velocitat impressora = 24 fulls SRA3/min (1.440 fulls/hora)
- Factor de click per defecte = **1,0** (ajustable segons volum)

### Paper
- Superfície SRA3 = 0,144 m²
- Cost paper interior (90-170 g) = **1,54 €/kg** (òfset) o **1,75 €/kg** (estucat)
- Cost paper coberta (200-350 g) = **1,90 €/kg** (estucat)
- Cobertes per full SRA3 = 2

### Preparació documents (imposició)
- Temps base per feina = 15 minuts
- Cost preparació base = **8,27 €** (15 min × 33,08 €/h)
- Per cada model addicional = +5 minuts (+2,76 €)
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
- Unitats addicionals per prova = **4 unitats per model** (2 fulls SRA3 per model)
- S'aplica per separat a interior i coberta
- NO es factura al client

### Marge de benefici
- Escalat segons volum i tipus de client (veure apartat 6)

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


On `Cost_click` = 0,03966 € (color) o 0,00556 € (B/N) segons correspongui.

### 4.5 Enquadernació rústica fresada
Cost_enquadernació = (Unitats_producció × 1,82) + 12,00 €


*(Nota: no hi ha temps de plegat/grapat perquè l'enquadernació és externa.)*

### 4.7 Preparació (imposició)
Cost_preparació = 8,27 € + (Nombre_models - 1) × 2,76 €


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

**Dades:** 50 unitats, 1 model, factor click 1,0, marge 50%

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 50 + 4 | 54 |
| Fulls interior | 54 × (108/8) | 729 |
| Fulls coberta | 54 × (4/8) | 27 |
| Total fulls SRA3 | 729 + 27 | 756 |
| Cost paper interior | 729 × (0,080×0,144×1,54) | 12,94 € |
| Cost paper coberta | 27 × (0,250×0,144×1,90) | 1,85 € |
| Cost impressió (×1,0) | 756 × 2 × 0,03966 | 59,97 € |
| Cost enquadernació | (54 × 1,82) + 12,00 | 110,28 € |
| Electricitat | (756/1440)×4,5×0,15 | 0,35 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **202,32 €** |
| **PREU VENDA (+50%)** | 202,32 × 1,50 | **303,48 €** |
| **PREU PER UNITAT** | 303,48 / 50 | **6,07 €** |

**Gruix llom:** 54 fulls interiors × 0,1 mm + 0,25 mm coberta ≈ 5,65 mm ✅

### 5.2 Llibret 140 pàgines (coberta color 250 g + interior color 80 g òfset)

**Dades:** 50 unitats, 1 model, factor click 1,0, marge 50%

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 50 + 4 | 54 |
| Fulls interior | 54 × (136/8) | 918 |
| Fulls coberta | 54 × (4/8) | 27 |
| Total fulls SRA3 | 918 + 27 | 945 |
| Cost paper interior | 918 × (0,080×0,144×1,54) | 16,29 € |
| Cost paper coberta | 27 × (0,250×0,144×1,90) | 1,85 € |
| Cost impressió (×1,0) | 945 × 2 × 0,03966 | 74,96 € |
| Cost enquadernació | (54 × 1,82) + 12,00 | 110,28 € |
| Electricitat | (945/1440)×4,5×0,15 | 0,44 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **215,75 €** |
| **PREU VENDA (+50%)** | 215,75 × 1,50 | **323,63 €** |
| **PREU PER UNITAT** | 323,63 / 50 | **6,47 €** |

**Gruix llom:** 68 fulls interiors × 0,1 mm + 0,25 mm coberta ≈ 7,05 mm ✅

---

## 6. PROPOSTA DE MARGE ESCALAT

| Escenari | Marge | 112 pàg. (50 u.) | 140 pàg. (50 u.) | Comentari |
|----------|-------|------------------|------------------|-----------|
| **Cost pur** | 0% | 202,32 € | 215,75 € | Referència interna |
| **Marge mínim** (volum) | 40% | 283,25 € | 302,05 € | Competitiu |
| **Marge estàndard** (client habitual) | 50% | 303,48 € | 323,63 € | Referència |
| **Marge recomanat** (comanda petita) | 75% | 354,06 € | 377,56 € | Cobreix costos comercials |
| **Marge premium** (urgència) | 100% | 404,64 € | 431,50 € | Comandes especials |
| **Marge alt** (client nou) | 150% | 505,80 € | 539,38 € | Màxim recomanat |

---

## 7. NOTES

1. Aquest procediment s'utilitza per a **gruixos de llom ≥ 4,5-5 mm**. Per a gruixos inferiors, usar el procediment de grapat.
2. El guillotinat a 3 cantos de l'enquadernador substitueix el guillotinat previ del procediment de grapat.
3. No hi ha plegat automàtic: els plecs els gestiona l'enquadernador.
4. La posada en màquina (12 €) és un cost fix per comanda.
5. Si el gruix del llom supera 1 cm, cal consultar sobrecost amb l'enquadernador.
6. El cost de click color SRA3 (0,03966 €/cara) i B/N SRA3 (0,00556 €/cara) són els valors reals del fitxer `costosOperatius2026.md`.
7. Per a **blanc i negre sobre A4 en línia**, usar `procedimentLlibretsA5GrapatsBNEnLinia.md`.
8. Per a **color sobre SRA3 grapat**, usar `procedimentLlibretsA5GrapatsColor.md`.
9. El marge s'aplica al final sobre el cost total de producció.

---

## FI DEL PROCEDIMENT (VERSIÓ 1.1)
