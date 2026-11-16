> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

📄 PROCEDIMENT: LLIBRETS A5 GRAPATS A COLOR (SRA3)
Fitxer: procedimentLlibretsA5GrapatsColor.md

markdown
# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A5 GRAPATS A COLOR (SRA3)

**VERSIÓ:** 5.0  
**DATA:** 2026-11-16  
**TIPUS:** Impressió color SRA3 + plegat i grapat  
**Marge per defecte:** escalat (50% - 200%)  
**Substitueix:** Versió 4.0 (actualització de costos reals)

---

## 1. OBJECTIU

Càlcul de costos per a llibrets A5 grapats, impresos **en color sobre SRA3** (8 pàgines A5 per full SRA3, 4 per cara), amb plegat i grapat.

Aquest procediment és per a **color sobre SRA3**. Per a **blanc i negre sobre A4 en línia**, usar el procediment `procedimentLlibretsA5GrapatsBNEnLinia.md`.

---

## 2. ESTRUCTURA FÍSICA DEL PRODUCTE

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
- Cost per click color SRA3 = **0,03966 €/cara**
- Velocitat impressora = 24 fulls SRA3/min (1.440 fulls/hora)
- Factor de click per defecte = **1,0** (ajustable segons volum)

### Paper
- Superfície SRA3 = 0,144 m²
- Cost paper estucat 135 g = **1,75 €/kg** (interior)
- Cost paper estucat 250 g = **1,90 €/kg** (coberta)
- Cobertes per full SRA3 = 2

### Preparació documents (imposició)
- Temps base per feina = 15 minuts
- Cost preparació base = **8,27 €** (15 min × 33,08 €/h)
- Per cada model addicional = +5 minuts (+2,76 €)
- Cost hora = 33,08 €/hora

### Guillotinat previ
- Preparació fixa = 5 minuts
- Processament = 3 minuts / 500 fulls SRA3
- Temps mínim = 10 minuts
- Cost hora = 27,78 €/hora

### Plegat i grapat
- Preparació base (8 pàgines) = 15 minuts
- Increment = +3 minuts / cada 4 pàgines addicionals
- Límit automàtic = 32 pàgines A5
- Velocitat producció = 1.000 revistes/hora
- Cost hora = 39,65 €/hora
- Cost grapa (amortitzada) = **0,0065333 €**
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
Cost_impressió = Fulls_SRA3_totals × 2 × 0,03966 € × Factor_click


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
Cost_grapes = Unitats_producció × 2 × 0,0065333 €


### 4.8 Electricitat + manteniment
Cost_electricitat = Temps_total_plegat × 4,5 × 0,15 €
Cost_manteniment = 2,00 €


### 4.9 Preparació (imposició)
Cost_preparació = 8,27 € + (Nombre_models - 1) × 2,76 €


### 4.10 Manipulat
Cost_manipulat = (Nombre_models × 5 / 60) × 19,93 €


### 4.11 Transport
Cost_transport = 5,00 €


### 4.12 Cost total i preu de venda
COST TOTAL PRODUCCIÓ = Cost_paper_total + Cost_impressió + Cost_guillotinat

Cost_plegat/grapat + Cost_grapes + Cost_electricitat

Cost_manteniment + Cost_preparació + Cost_manipulat

Cost_transport

PREU VENDA CLIENT = COST TOTAL PRODUCCIÓ × (1 + Marge)
PREU PER UNITAT = PREU VENDA CLIENT / Unitats_client


### 4.13 Temps d'impressió
Temps_impressió (minuts) = (Fulls_SRA3_totals / 1440) × 60


---

## 5. EXEMPLE VERIFICAT (400 unitats, 24 pàgines, 1 model, factor 1,0)

**Dades:**
- Unitats_client = 400
- Pàgines coberta = 4 (250 g)
- Pàgines interior = 20 (135 g)
- Nombre_models = 1
- Factor_click = 1,0

**Càlculs:**

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 400 + 4 | 404 |
| Fulls interior | 404 × (20/8) | 1.010 |
| Fulls coberta | 404 × (4/8) | 202 |
| Total fulls SRA3 | 1.010 + 202 | 1.212 |
| Cost paper interior | 1.010 × (0,135 × 0,144 × 1,75) | 34,36 € |
| Cost paper coberta | 202 × (0,250 × 0,144 × 1,90) | 13,82 € |
| Cost impressió | 1.212 × 2 × 0,03966 | 96,13 € |
| Cost guillotinat | (14/60) × 27,78 | 6,48 € |
| Cost plegat/grapat | 0,854 × 39,65 | 33,86 € |
| Cost grapes | 404 × 2 × 0,0065333 | 5,28 € |
| Electricitat | 0,854 × 4,5 × 0,15 | 0,58 € |
| Manteniment | fix | 2,00 € |
| Preparació | fix | 8,27 € |
| Manipulat | (1×5/60)×19,93 | 1,66 € |
| Transport | fix | 5,00 € |
| **COST TOTAL** | | **207,44 €** |
| **COST PER UNITAT** | 207,44 / 400 | **0,519 €** |

**Temps d'impressió:**
(1.212 / 1440) × 60 = 50,5 minuts ≈ 51 minuts


---

## 6. PROPOSTA DE MARGE ESCALAT

| Escenari | Marge | Preu total | Preu/unitat | Comentari |
|----------|-------|------------|-------------|-----------|
| **Cost pur** | 0% | 207,44 € | 0,519 € | Referència interna |
| **Marge mínim** (volum, client fidel) | 40% | 290,42 € | 0,726 € | Competitiu |
| **Marge estàndard** (client habitual) | 50% | 311,16 € | 0,778 € | Referència |
| **Marge recomanat** (comanda petita) | 75% | 363,02 € | 0,908 € | Cobreix costos comercials |
| **Marge premium** (urgència) | 100% | 414,88 € | 1,037 € | Comandes especials |
| **Marge alt** (client nou) | 150% | 518,60 € | 1,297 € | Màxim recomanat |

---

## 7. NOTES

1. Aquest procediment és **exclusiu per a color sobre SRA3**.
2. Per a **blanc i negre sobre A4 en línia**, usar `procedimentLlibretsA5GrapatsBNEnLinia.md`.
3. Per a **enquadernació rústica fresada**, usar `procedimentLlibretsA5RusticaFresada.md`.
4. El cost de click color SRA3 (0,03966 €/cara) és el valor real del fitxer `costosOperatius2026.md`.
5. La preparació base és de 15 minuts (8,27 €); cada model addicional suma 5 minuts (2,76 €).
6. El guillotinat previ s'aplica al total de fulls SRA3 (interior + coberta).
7. El plegat/grapat es calcula sobre el total de pàgines A5 del producte.
8. Si el producte supera les 32 pàgines, cal consultar com gestionar els plecs addicionals.
9. El marge s'aplica al final sobre el cost total de producció.

---

## FI DEL PROCEDIMENT (VERSIÓ 5.0)
