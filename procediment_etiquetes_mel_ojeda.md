# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ D'ETIQUETES PER A POTS DE MEL (DÍPTIC DESPLEGAT)

**VERSIÓ:** 1.0  
**DATA:** 2026-07-27  
**TIPUS PRODUCTE:** Etiqueta díptic desplegat 120×40 mm, sense plegar, amb dos forats per a cordonet

---

## 1. OBJECTIU

Càlcul de costos per a etiquetes en format díptic (obert 120×40 mm) impreses en blanc i negre a doble cara sobre cartolina òfset de 185g en color groc.

L'etiqueta s'entrega desplegada, fendida (marca de doblec), tallada a mida final i amb dos forats per passar-hi un cordonet que subjecta l'etiqueta al coll de l'envàs de mel.

---

## 2. ESTRUCTURA FÍSICA DEL PRODUCTE

| Concepte | Dada |
|----------|------|
| Format final (desplegat) | 120 × 40 mm |
| Format de màquina (SRA3+) | 488 × 320 mm |
| Etiquetes per full de màquina | 24 (matriu 6×4) |
| Impressió | Doble cara, blanc i negre |
| Material | Cartolina òfset 185g (groc) |

**Relació de compra:**
- 1 full de compra (500 × 650 mm) = 2 fulls de màquina (488 × 320 mm)
- 1 full de compra = 48 etiquetes finals
- 1 paquet = 125 fulls de compra

---

## 3. PARÀMETRES FIXOS

### 3.1 Paper (òfset 185g groc)

| Concepte | Valor |
|----------|-------|
| Preu paquet (125 fulls 500×650) | 25,50 € |
| Preu full de compra | 0,204 € |
| Preu per etiqueta (material) | 0,00425 € |
| Fulls de compra per full de màquina | 2 |

### 3.2 Impressió B/N en format 488×320 (doble cara)

| Concepte | Valor |
|----------|-------|
| Cost click base B/N | 0,003252 € |
| Plus per mida gran (488×320) | 0,002308 € |
| Cost per cara | 0,005560 € |
| **Cost per full (2 cares)** | **0,011120 €** |
| **Cost per etiqueta (impressió)** | **0,0004633 €** |
| **Factor multiplicador client (8x)** | Aplicat al cost d'impressió |

### 3.3 Mà d'obra

| Concepte | Cost/hora |
|----------|-----------|
| Preparació / Imposició | 33,08 € |
| Guillotinat | 27,78 € |
| Fendidora | 31,70 € |
| Perforació | 26,50 € |
| Manipulat / Empaquetatge | 19,93 € |

### 3.4 Maculatura

| Concepte | Valor |
|----------|-------|
| Fulls de prova per comanda | 4 fulls de màquina (488×320) |
| Equivalent etiquetes | 96 unitats |

### 3.5 Empaquetatge

| Concepte | Valor |
|----------|-------|
| Gometa elàstica | 0,02 €/unitat (cada 200 etiquetes) |
| Plàstic retràctil + energia | 0,10 €/paquet (cada 200 etiquetes) |
| Operari empaquetatge | 5 minuts/model |

### 3.6 Transport

| Concepte | Valor |
|----------|-------|
| Cost per comanda | 5,00 € |

### 3.7 Marge comercial

| Concepte | Valor |
|----------|-------|
| Marge sobre el total (després del factor 8x) | 50% |

---

## 4. FÓRMULES

### 4.1 Fulls de màquina per model
Fulls_màquina_i = CEIL(U_i / 24)

text

On:
- `U_i` = Unitats (etiquetes) del model i
- `CEIL` = arrodoniment a l'enter superior

### 4.2 Total fulls de màquina (amb maculatura)
Fulls_totals = Σ Fulls_màquina_i + 4

text

La maculatura (4 fulls) es reparteix proporcionalment entre tots els models.

### 4.3 Fulls de compra
Fulls_compra = CEIL(Fulls_totals / 2)

text

### 4.4 Cost paper
Cost_paper_total = Fulls_compra × 0,204

text

**Repartiment per model:** Proporcional als fulls de màquina de cada model.

### 4.5 Preparació fitxers (imposició)
Cost_preparació_model_i =
Si i = 1: (15/60) × 33,08 = 8,27 €
Si i ≥ 2: (5/60) × 33,08 = 2,7567 €

text

### 4.6 Tall previ (500×650 → 488×320)
Cost_tall_previ_total = (10/60) × 27,78 = 4,63 €
Repartiment: 4,63 / N (per model)

text

### 4.7 Impressió
Cost_impressió_model_i (base) = Fulls_màquina_i × 0,01112 €
Cost_impressió_total (base) = Fulls_totals × 0,01112 €

text

**Factor 8x:** S'aplica al cost d'impressió per obtenir el preu de venda d'aquesta part.
Increment_8x_total = Cost_impressió_total × 7
Increment_8x_model_i = Cost_impressió_model_i × 7

text

### 4.8 Tall a 3 etiquetes (guillotina)
Cost_tall_3_model_i = (5/60) × 27,78 = 2,315 €/model
Cost_tall_3_total = N × 2,315

text

### 4.9 Fendit (marca de doblec)

**Preparació (una vegada per comanda):**
Cost_prep_fendit = (10/60) × 31,70 = 5,283 €

text

**Producció:**
Temps_prod_fendit (h) = Fulls_totals / 2500
Cost_prod_fendit = Temps_prod_fendit × 31,70

text

**Repartiment per model:** Proporcional als fulls de màquina de cada model.

### 4.10 Tall final (120×40 mm)
Cost_tall_final_model_i = (5/60) × 27,78 = 2,315 €/model
Cost_tall_final_total = N × 2,315

text

### 4.11 Perforació (2 forats)

**Preparació (una vegada per comanda):**
Cost_prep_perforació = (5/60) × 26,50 = 2,208 €

text

**Producció:** (120 etiquetes acabades/minut)
Temps_prod_perforació (min) = (Σ U_i + 96) / 120
Temps_prod_perforació (h) = Temps_prod_perforació / 60
Cost_prod_perforació = Temps_prod_perforació (h) × 26,50

text

**Repartiment per model:** Proporcional a les unitats de cada model.

### 4.12 Empaquetatge
Cost_operari_model_i = (5/60) × 19,93 = 1,661 €/model

text

**Gometes i plàstic (total comanda):**
Paquets_totals = CEIL(Σ U_i / 200)
Cost_gometes = Paquets_totals × 0,02
Cost_plàstic = Paquets_totals × 0,10

text

**Repartiment per model:** Proporcional a les unitats de cada model.

### 4.13 Transport
Cost_transport_total = 5,00 €
Repartiment per model: Proporcional a les unitats de cada model.

text

### 4.14 Càlcul del preu final

**Base per al marge (amb factor 8x ja aplicat):**
Base_model_i = Cost_producció_model_i + Increment_8x_model_i
Base_total = Σ Base_model_i

text

**Aplicació del marge:**
Preu_final_total = Base_total × 1,50
Preu_final_model_i = Base_model_i × 1,50
Preu_per_etiqueta = Preu_final_total / Σ U_i

text

---

## 5. EXEMPLE VERIFICAT

**Dades:**
- N = 6 models
- U = [2000, 2000, 3000, 2000, 3000, 3000]
- Total unitats = 15.000

**Resultats:**

| Model | Unitats | Fulls màq. | Cost producció | Increment 8x | Base marge | Preu final | Preu/etiqueta |
|-------|---------|------------|----------------|--------------|------------|------------|---------------|
| M1 | 2.000 | 85 | 35,96 € | 6,62 € | 42,58 € | 63,87 € | 0,03194 € |
| M2 | 2.000 | 85 | 30,45 € | 6,62 € | 37,07 € | 55,61 € | 0,02781 € |
| M3 | 3.000 | 126 | 41,36 € | 9,81 € | 51,17 € | 76,76 € | 0,02559 € |
| M4 | 2.000 | 85 | 30,45 € | 6,62 € | 37,07 € | 55,61 € | 0,02781 € |
| M5 | 3.000 | 126 | 41,36 € | 9,81 € | 51,17 € | 76,76 € | 0,02559 € |
| M6 | 3.000 | 126 | 41,36 € | 9,81 € | 51,17 € | 76,76 € | 0,02559 € |
| **TOTAL** | **15.000** | **633** | **220,94 €** | **49,27 €** | **270,21 €** | **405,32 €** | **0,02702 €** |

---

## 6. RESUM DE PARÀMETRES EN TAULA

| Concepte | Cost / Fórmula | Observacions |
|----------|----------------|--------------|
| Paper per etiqueta | 0,00425 € | Material base |
| Impressió per full (2 cares) | 0,01112 € | B/N en 488×320 |
| Preparació fitxers (1r model) | 8,27 € | 15 minuts |
| Preparació fitxers (extra) | 2,7567 € | 5 minuts/model |
| Tall previ (comanda) | 4,63 € | Repartit entre models |
| Tall a 3 etiquetes | 2,315 €/model | Guillotina |
| Fendit (preparació) | 5,283 € | Una vegada per comanda |
| Fendit (producció) | 31,70 €/h × (Fulls/2500) | Repartit proporcional |
| Tall final | 2,315 €/model | Guillotina |
| Perforació (preparació) | 2,208 € | Una vegada per comanda |
| Perforació (producció) | 26,50 €/h × (Etiquetes/120) | 2 forats, repartit proporcional |
| Empaquetatge (operari) | 1,661 €/model | 5 minuts/model |
| Empaquetatge (materials) | 0,12 €/paquet de 200 | Gometa + plàstic |
| Transport | 5,00 € | Per comanda |
| Factor client (8x) | Cost_impressió × 7 | S'aplica a la impressió |
| Marge | 50% | Sobre el total amb factor 8x |

---

## 7. LLISTA DE CONTROL PER EVITAR ERRORS

- [ ] He comptat bé el nombre de models (N)?
- [ ] He calculat CEIL(U_i / 24) per a cada model?
- [ ] He afegit els 4 fulls de maculatura al total?
- [ ] He repartit la maculatura proporcionalment entre models?
- [ ] He calculat CEIL(Fulls_totals / 2) per als fulls de compra?
- [ ] He aplicat el factor 8x NOMÉS a la impressió (×7 d'increment)?
- [ ] He repartit els costos de preparació (fendit, perforació) entre tots els models?
- [ ] He aplicat el tall a 3 i tall final a CADA model (2,315 €/model)?
- [ ] He aplicat el marge del 50% al FINAL (després del factor 8x)?
- [ ] He sumat CADA model individualment abans de fer el total?

---

## 8. REFERÈNCIES A COSTOS OPERATIUS

Aquest procediment utilitza les següents referències del fitxer `costos_operatius.md`:

| Referència | Valor utilitzat |
|------------|-----------------|
| `preparacio_imposicio` | 33,08 €/h |
| `guillotinat` | 27,78 €/h |
| `manipulat_empaquetat` | 19,93 €/h |
| `foradat` | 26,50 €/h |
| `electricitat_kWh` | 0,15 € |
| `transport_per_comanda` | 5,00 € |

**Paràmetre afegit específicament per a aquest procediment:**
[fendidora]
cost_hora = 31,70 €/h

text

---

## 9. NOTES IMPORTANTS

1. **Maculatura:** Els 4 fulls de prova són per a TOTA la comanda, no per model. Es reparteixen proporcionalment entre tots els models.

2. **Factor 8x:** És un multiplicador que s'aplica al COST d'impressió per convertir-lo en PREU DE VENDA d'aquesta part. No s'aplica a cap altre concepte.

3. **Ordre de càlcul:** 
   - Costos reals de producció
   - + Factor 8x (increment sobre impressió)
   - = Base per al marge
   - × 1,50 (marge 50%)
   - = Preu final

4. **Empaquetatge:** Les gometes elàstiques i el plàstic retràctil es compten per paquets de 200 etiquetes. L'operari d'empaquetatge es compta per model (5 minuts/model).

5. **Forats:** La perforació es fa en dues passades (un forat cada vegada). La velocitat de 120 etiquetes/minut JA inclou les dues passades (és a dir, etiquetes acabades amb els dos forats).

---

## FI DEL PROCEDIMENT
