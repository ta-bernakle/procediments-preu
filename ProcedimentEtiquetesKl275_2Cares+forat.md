# PROCEDIMENT ESTÀNDARD: CÀLCUL D'ETIQUETES KRAFTLINER 275 g - 4+4 + FORADAT

## 📌 DESCRIPCIÓ DEL PRODUCTE
- Producte: Etiquetes quadrades (50 × 50 mm) en cartonet **Kraftliner 275 g/m²**
- Impressió: **4+4** (doble cara, a tot color)
- Acabat: **Guillotinat** a mida final + **foradat de 3 mm** en un cantó
- Material: Cartonet Kraftliner 275 g/m² (proveït en fulls de fabricant 750 × 1050 mm)

---

## ⚙️ MAQUINÀRIA I OPERACIONS
1. **Guillotinat previ:** tall del full de fabricant (750 × 1050 mm) en 4 fulls SRA3 (320 × 450 mm).
2. **Impressió digital** (Xerox Versant o similar) a doble cara (4+4).
3. **Guillotinat final:** tall dels fulls SRA3 en etiquetes individuals (50 × 50 mm).
4. **Foradat:** perforació de 3 mm de diàmetre en un cantó de cada etiqueta.
5. **Manipulat:** compactació i organització en piles.
6. **Preparació documents:** imposició dels 4 models (si escau).

---

## 📐 PARÀMETRES FIXOS

### Paper Kraftliner 275 g/m²
- Cost paper = **1,50 €/kg**
- Gramatge = **275 g/m²** (0,275 kg/m²)
- Dimensions full fabricant = **750 × 1.050 mm** (0,7875 m²)
- Pes per full fabricant = 0,7875 × 0,275 = **0,2165625 kg**
- Cost per full fabricant = 0,2165625 × 1,50 = **0,32484375 €**

### Format SRA3 (320 × 450 mm)
- Superfície = 0,144 m²
- Rendiment per SRA3 = **48 etiquetes** (6 files × 8 columnes) per a mida 50×50 mm
- Fulls SRA3 per full fabricant = **4**

### Etiquetes per full fabricant
- 4 SRA3 × 48 etiquetes = **192 etiquetes/full fabricant**

### Maculatura
- Maculatura per model = **6 fulls SRA3** (a càrrec del client, inclosos en el preu)
- 4 models → 24 fulls SRA3 de maculatura

### Impressió (4+4)
- Cost per clic (cara) per full SRA3 = **0,059 €**
- Impressió: **Doble cara (4+4)** → 2 clics per full
- Factor multiplicador (5x) = **5** → substitueix el 2,5 habitual
- Cost per full SRA3 = 0,059 × 2 × 5 = **0,59 €/full SRA3**

### Guillotinat previ (tall fabricant → SRA3)
- Preparació fixa = **5 minuts**
- Temps per 500 fulls = **3 minuts**
- Cost hora = **27,78 €/h**

### Guillotinat final (tall SRA3 → etiquetes individuals)
- Inclòs en el temps de guillotinat previ (es fa en la mateixa operació).

### Foradat (diàmetre 3 mm)
- Velocitat = **150 etiquetes/minut**
- Cost hora = **26,50 €/h**

### Manipulat (compactació i organització)
- Temps per pila (100 fulls SRA3) = **5 minuts**
- Cost hora = **19,93 €/h**

### Preparació documents (imposició)
- Temps base per primer model = **15 minuts**
- Models addicionals = +**5 minuts** per model
- Cost hora = **33,08 €/h**

### Transport
- Cost per comanda = **5,00 €** (per defecte, pot variar)

---

## 🧮 FÓRMULES DE CÀLCUL

### 1. Fulls SRA3 necessaris (tirada neta)
Fulls_SRA3_neta = CEILING(Unitats_client / 48)


### 2. Maculatura
Maculatura_SRA3 = Nombre_models × 6


### 3. Total fulls SRA3
Total_SRA3 = Fulls_SRA3_neta + Maculatura_SRA3


### 4. Fulls fabricant necessaris
Fulls_fabricant = CEILING(Total_SRA3 / 4)


### 5. Cost paper
Cost_paper = Fulls_fabricant × 0,32484375


### 6. Cost impressió
Cost_impressió = Total_SRA3 × 0,59
*(0,59 = 0,059 × 2 × 5)*

### 7. Cost guillotinat previ
Temps_guillotinat_min = MÀXIM(10, 5 + (Total_SRA3 / 500) × 3)
Cost_guillotinat = (Temps_guillotinat_min / 60) × 27,78


### 8. Cost foradat
Temps_foradat_min = Unitats_client / 150
Cost_foradat = (Temps_foradat_min / 60) × 26,50


### 9. Cost manipulat
Piles = CEILING(Total_SRA3 / 100)
Temps_manipulat_min = Piles × 5
Cost_manipulat = (Temps_manipulat_min / 60) × 19,93


### 10. Cost preparació
Cost_preparació = (15 + (Nombre_models - 1) × 5) / 60 × 33,08


### 11. Cost transport
Cost_transport = 5,00


### 12. Cost total
Cost_total = Cost_paper + Cost_impressió + Cost_guillotinat +
Cost_foradat + Cost_manipulat + Cost_preparació + Cost_transport


### 13. Preu de venda
Preu_venda = Cost_total / (1 - Marge)
Preu_unitari = Preu_venda / Unitats_client


---

## 📊 EXEMPLE DE CÀLCUL (per a 10.480 unitats, 4 models, marge 50%)

| Paràmetre | Valor |
|-----------|-------|
| Unitats client | 10.480 |
| Models | 4 |
| Marge | 50% |

### Passos:

1. **Fulls SRA3 nets:** CEILING(10.480 / 48) = CEILING(218,33) = **219**
2. **Maculatura:** 4 × 6 = **24**
3. **Total SRA3:** 219 + 24 = **243**
4. **Fulls fabricant:** CEILING(243 / 4) = CEILING(60,75) = **61**

### Costos:

| Concepte | Càlcul | Cost |
|----------|--------|------|
| **Paper** | 61 × 0,32484375 | 19,82 € |
| **Impressió (4+4)** | 243 × 0,59 | 143,37 € |
| **Guillotinat previ** | MÀXIM(10, 5 + (243/500)×3) = 10 min → (10/60)×27,78 | 4,63 € |
| **Foradat** | (10.480/150) = 69,87 min → (70/60)×26,50 | 30,92 € |
| **Manipulat** | CEILING(243/100) = 3 piles → (3×5)/60 × 19,93 | 4,98 € |
| **Preparació** | (15 + 3×5) = 30 min → (30/60)×33,08 | 16,54 € |
| **Transport** | - | 5,00 € |
| **TOTAL COST** | | **225,26 €** |

### Preu final:
- Preu venda = 225,26 / (1 - 0,50) = **450,52 €**
- Preu unitari = 450,52 / 10.480 = **0,0430 €/u**

---

## 📋 CHECKLIST PER A L'ASSISTENT (IA)

Quan rebi aquest procediment, he de:
- [ ] Demanar la **tirada (unitats)**.
- [ ] Demanar el **nombre de models**.
- [ ] Demanar el **marge de benefici** (%).
- [ ] Aplicar les fórmules i retornar:
  - Cost total
  - Preu de venda
  - Preu per unitat
- [ ] Si hi ha alguna variació (com ara mida d'etiqueta diferent), recalcular el rendiment per SRA3.

---

## 📝 NOTES

- El factor **5x** substitueix el 2,5 habitual per a la impressió. Aquest factor ja inclou electricitat, manteniment, tòner i imprevistos.
- El foradat és de **3 mm de diàmetre**. Si el diàmetre és diferent, la velocitat de foradat pot variar.
- El transport és de **5 €** per comanda. Si la distància és major, s'ha d'ajustar.

---

**FI DEL PROCEDIMENT**
