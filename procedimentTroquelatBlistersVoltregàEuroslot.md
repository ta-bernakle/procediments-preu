# PROCEDIMENT: BLISTER DÍPTIC AMB EUROSLOT (TROQUELAT EN 2 PASSES SOLIDÀRIES)

## 📌 Descripció del producte
- Blister de cartonet en forma de díptic plegat pel mig.
- Dos forats euroslot per penjar en expositor.
- Sense film de visualització.
- Impressió 4+0 (una cara).

## ⚙️ Maquinària i operacions
1. **Impressió digital** (Xerox Versant)
2. **Fendit previ** (màquina fendidora) - *OPCIONAL, depèn de la tirada*
3. **Troquelat** (Heidelberg d'aspes)
4. **Destroquelat manual** (extracció dels euroslots)
5. **Comptatge, agrupació i encaixat**

## 📐 Dades necessàries per al pressupost
| Paràmetre | Unitat | Exemple |
|-----------|--------|---------|
| Tirada | unitats | 5.000 |
| Mida del blister (desplegat) | mm | 116 x 155 |
| Gramatge del cartonet | g/m² | 250 |
| Format de full de màquina | mm | 520 x 720 |
| Peces per full | unitats | 12 |
| Peces per forma d'impressió | unitats | 6 |

## 💰 COSTOS UNITAIS I TEMPS ESTÀNDARD (fixos per a aquest procediment)

### Matèria primera (cartonet)
- Preu del full (520x720) = **0,14442 €/full**
- Peces per full = 12
- **Cost cartonet per peça = 0,14442 / 12 = 0,012035 €/u**

### Impressió digital (Xerox Versant)
- Cost per full de màquina (6 peces) = **0,059 €** (base)
- Factor multiplicador (electricitat, manteniment, imprevistos) = **2,5**
- **Cost imprès per full = 0,059 × 2,5 = 0,1475 €/full**
- **Cost impressió per peça = 0,1475 / 6 = 0,02458 €/u**

### Fendit (màquina fendidora) - *si s'aplica*
- Muntatge = 10 min (0,167 h) × 31,70 €/h = **5,29 €** (fix per comanda)
- Velocitat = 2.500 fulls/h
- Cost variable = (tirada / 2.500) × 31,70 €

### Troquelat (Heidelberg d'aspes)
- Muntatge = 15 min (0,25 h) × 31,70 €/h = **7,93 €** (fix per comanda)
- Velocitat = 2.000 fulls/h
- Cost variable = (tirada / 2.000) × 31,70 €
- **Nota:** L'operari treballa les màquines de fendit i troquel de manera solidària. Quan aquesta opció s'aplica, el cost del fendit es considera **0 €** a efectes de pressupost.

### Destroquelat manual (extracció euroslots)
- Velocitat = 10.000 peces/h
- Cost = 19,93 €/h
- Cost variable = (tirada / 10.000) × 19,93 €

### Comptatge, agrupació i encaixat
- Temps fix = 15 min (0,25 h) × 19,93 €/h = **4,98 €** (per comanda)

### Ports i despeses
- Transport = **5,00 €** (fix per comanda)

---

## 🧮 FÓRMULA DE CÀLCUL

Per a una tirada de **N** unitats:
Fulls necessaris = CEIL(N / 12)
Cost cartonet = fulls × 0,14442
Cost impressió = CEIL(N / 6) × 0,1475
Cost troquelat = 7,93 + (N / 2.000) × 31,70
Cost destroquelat = (N / 10.000) × 19,93
Cost manipulat = 4,98
Cost ports = 5,00

COST TOTAL = (suma anterior)

Preu de venda (amb marge M) = COST TOTAL / (1 - M)

text

**Observació:** El fendit s'inclou al cost del troquelat SI l'operari treballa en seqüència. Si treballa en solidari (les dues màquines alhora), el cost del fendit = 0 €.

---

## 📊 EXEMPLE DE CÀLCUL (per a 5.000 unitats, sense fendit, marge 40%)

| Concepte | Càlcul | Cost |
|----------|--------|------|
| Cartonet | CEIL(5.000/12)=417 × 0,14442 | 60,22 € |
| Impressió | CEIL(5.000/6)=834 × 0,1475 | 123,02 € |
| Troquelat | 7,93 + (5.000/2.000)×31,70 | 87,18 € |
| Destroquelat | (5.000/10.000)×19,93 | 9,97 € |
| Manipulat | 4,98 € | 4,98 € |
| Ports | 5,00 € | 5,00 € |
| **TOTAL COST** | | **290,37 €** |
| **Preu venda (40%)** | 290,37 / 0,60 | **483,95 €** |
| **Preu unitari** | 483,95 / 5.000 | **0,0968 €/u** |

---

## ✅ CHECKLIST PER A L'ASSISTENT (IA)
Quan rebi aquest procediment, he de:
- [ ] Demanar la **tirada (N)**.
- [ ] Demanar si el **fendit es fa en solidari o en seqüència** (per aplicar cost 0 o no).
- [ ] Demanar el **marge de benefici** desitjat.
- [ ] Aplicar la fórmula i retornar cost total + preu unitari + preu de venda final.
