> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

📄 PROCEDIMENT: LLIBRETS A5 GRAPATS EN BLANC I NEGRE (IMPRESSIÓ A4 EN LÍNIA)
Fitxer: procedimentLlibretsA5GrapatsBNEnLinia.md

markdown
# PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE LLIBRETS A5 GRAPATS EN BLANC I NEGRE (A4 EN LÍNIA)

**VERSIÓ:** 1.1  
**DATA:** 2026-11-16  
**TIPUS:** Impressió A4 B/N + plegat i grapat en línia  
**Marge per defecte:** escalat (50% - 300%)  
**Substitueix:** Procediment antic "CÀLCUL D'IMPRESSIÓ DE MANUALS A5 GRAPATS" (marcat com a obsolet)

---

## 1. OBJECTIU

Càlcul de costos per a llibrets A5 grapats, impresos **en blanc i negre sobre A4** (4 pàgines A5 per full A4), amb **plegat i grapat en línia** a la mateixa màquina d'imprimir.

Aquest procediment **no inclou**:
- Guillotinat (la màquina plega directament a A5)
- Plegat/grapat extern (es fa en línia)
- Electricitat ni manteniment addicional (inclòs en el cost de click)

---

## 2. ESTRUCTURA FÍSICA DEL PRODUCTE

- 1 full A4 = 4 pàgines A5 (2 per cara, a doble cara)
- Cada llibret de 20 pàgines A5 = **5 fulls A4**
- La màquina imprimeix, plega i grapa en línia (1 segon per unitat aprox.)

**Exemple per a 20 pàgines totals:**

| Component | Pàgines A5 | Fulls A4 per unitat |
|-----------|------------|---------------------|
| Llibret   | 20         | 20/4 = 5            |
| **Total** | **20**     | **5**               |

---

## 3. PARÀMETRES FIXOS

### Impressió A4 B/N
- Cost per click A4 B/N = **0,003061 €/cara**
- Sense factor de multiplicació (1,0×)
- Velocitat duplex = **4.460 fulls A4/hora**

### Paper
- Cost per full A4 = **0,0064 €** (preu real de lot, òfset 80 g)
- Superfície A4 = 0,06237 m² (referència)

### Preparació (imposició)
- Temps per document = **5 minuts**
- Cost preparació per document = **2,7567 €**

### Post processament (fulletons/embalatge/expedició)
- Temps per document = **3 minuts**
- Cost post processament per document = **0,9965 €**

### Grapes
- Cost per grapa (amortitzada) = **0,0065333 €**
- Grapes per manual = 2

### Transport
- Cost per comanda (entrega única) = 5,00 €

### Maculatura
- Unitats addicionals per prova = **4 unitats per model**
- S'aplica al tiratge real per calcular costos
- NO es factura al client

### Marge de benefici
- Escalat segons volum i tipus de client (veure apartat 6)

---

## 4. FÓRMULES

### 4.1 Maculatura
Unitats_producció = Unitats_client + (Nombre_models × 4)


### 4.2 Fulls A4 necessaris
Fulls_A4_per_unitat = Pàgines_A5 / 4
Fulls_A4_totals = Unitats_producció × Fulls_A4_per_unitat


### 4.3 Cost paper
Cost_paper = Fulls_A4_totals × 0,0064 €


### 4.4 Cost impressió
Cost_impressió = (Fulls_A4_totals × 2) × 0,003061 €


### 4.5 Preparació (imposició)
Cost_preparació = Nombre_de_documents_diferents × 2,7567 €


### 4.6 Post processament (fulletons/embalatge/expedició)
Cost_post_processament = Nombre_de_documents_diferents × 0,9965 €


### 4.7 Grapes
Cost_grapes = (Unitats_producció × 2) × 0,0065333 €


### 4.8 Transport
Cost_transport = 5,00 €


### 4.9 Cost total i preu de venda
COST TOTAL PRODUCCIÓ = Cost_paper + Cost_impressió + Cost_preparació

Cost_post_processament + Cost_grapes + Cost_transport

PREU VENDA CLIENT = COST TOTAL PRODUCCIÓ × (1 + Marge)
PREU PER UNITAT = PREU VENDA CLIENT / Unitats_client


### 4.10 Temps d'impressió (estimat)
Temps_impressió (minuts) = (Fulls_A4_totals / 4460) × 60


---

## 5. EXEMPLE VERIFICAT (120 unitats, 20 pàgines, 1 model)

**Dades:**
- Unitats_client = 120
- Pàgines_A5 = 20
- Nombre_models = 1

**Càlculs:**

| Concepte | Fórmula | Resultat |
|----------|---------|----------|
| Unitats producció | 120 + 4 | 124 |
| Fulls A4 per unitat | 20/4 | 5 |
| Fulls A4 totals | 124 × 5 | 620 |
| Cost paper | 620 × 0,0064 | 3,97 € |
| Cost impressió | (620 × 2) × 0,003061 | 3,80 € |
| Cost preparació | 1 × 2,7567 | 2,76 € |
| Cost post processament | 1 × 0,9965 | 1,00 € |
| Cost grapes | 124 × 2 × 0,0065333 | 1,62 € |
| Cost transport | fix | 5,00 € |
| **COST TOTAL** | | **18,15 €** |
| **COST PER UNITAT** | 18,15 / 120 | **0,151 €** |

**Temps d'impressió:**
(620 / 4460) × 60 = 8,34 minuts ≈ 8 minuts


---

## 6. PROPOSTA DE MARGE ESCALAT

Per a aquest producte, el cost per unitat és molt baix (0,151 €). El marge ha de compensar el temps comercial, el risc i la logística.

| Escenari | Marge | Preu total | Preu/unitat | Comentari |
|----------|-------|------------|-------------|-----------|
| **Cost pur** | 0% | 18,15 € | 0,151 € | Referència interna |
| **Marge mínim** (volum, client fidel) | 50% | 27,23 € | 0,227 € | Competitiu |
| **Marge estàndard** (client habitual) | 100% | 36,30 € | 0,303 € | Referència |
| **Marge recomanat** (comanda petita) | 150% | 45,38 € | 0,378 € | Cobreix costos comercials |
| **Marge premium** (urgència) | 200% | 54,45 € | 0,454 € | Comandes especials |
| **Marge alt** (client nou) | 300% | 72,60 € | 0,605 € | Màxim recomanat |

---

## 7. NOTES

1. Aquest procediment és **exclusiu per a blanc i negre** i impressió **A4 en línia**.
2. Per a **color sobre SRA3**, usar el procediment `procedimentLlibretsA5GrapatsColor.md`.
3. Per a **enquadernació rústica fresada**, usar el procediment `procedimentLlibretsA5RusticaFresada.md`.
4. El cost de click A4 B/N (0,003061 €/cara) inclou electricitat i manteniment de la màquina.
5. La preparació és de **5 minuts per document**.
6. El **post processament** (3 min = 0,9965 € per document) inclou fulletons, embalatge i expedició.
7. El marge s'aplica al final sobre el cost total de producció.
8. **Aquest procediment substitueix l'antic "CÀLCUL D'IMPRESSIÓ DE MANUALS A5 GRAPATS"**, que queda obsolet i es conserva a la carpeta `obsolets/` només com a referència històrica.

---

## FI DEL PROCEDIMENT (VERSIÓ 1.1)
