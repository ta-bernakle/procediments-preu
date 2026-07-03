# PROCEDIMENT ESTÀNDARD: CÀLCUL DE COSTOS DE PEÇES TROQUELADES
## Film de polièster - 50 µm (Peces petites)
### Marge comercial: 300% (preu = cost × 4)

---

## 1. DADES FIXES DEL MATERIAL

| Paràmetre | Valor | Unitat |
| :--- | :--- | :--- |
| Material | Film polièster 50 µm | - |
| Gramatge | 70 | g/m² |
| Densitat | 1.400 | kg/m³ |
| Rendiment | 14,2857 | m²/kg |
| Preu material | 9,45 | €/kg |
| Pes bobina sencera | 51,5 | kg |
| Cost ports per bobina | 20,00 | € |
| Amplada bobina | 450 | mm |
| Longitud de llesca (desenvolupament) | 230 | mm |
| Mida peça final | 115 × 112,5 | mm |
| Mida format (peça doble) | 230 × 112,5 | mm |
| Peces finals per llesca | 8 | unitats |
| Superfície per llesca | 0,1035 | m² |
| Superfície per peça final | 0,0129375 | m² |
| Pes per peça final | 0,000905625 | kg |

---

## 2. DADES DE COSTOS OPERATIUS (per hora)

| Concepte | Cost/hora (€/h) |
| :--- | :--- |
| Preparació troqueladora | 31,70 |
| Tiratge (picades) | 31,70 |
| Desbobinar | 19,93 |
| Tallar trossos | 27,73 |
| Destroquelar | 19,93 |
| Embalatge | 19,93 |

---

## 3. DADES FIXES DE COSTOS GENERALS

| Concepte | Import (€) |
| :--- | :--- |
| Transport a client | 5,00 |
| Gestió de comanda | 3,00 |
| Marge comercial | 300% |

---

## 4. MÈTRICA DE PRODUCCIÓ

| Paràmetre | Valor |
| :--- | :--- |
| Peces per picada de màquina | 2 |
| Picades per hora | 1.800 |
| Temps destroquelar | 5 min/miler |
| Merma estàndard | 30 peces |
| Temps desbobinar | 10 min / 2.000 peces |

---

## 5. PROCEDIMENT DE CÀLCUL PER A `N` PEÇES FINALS

### 5.1 Material

Peces totals a fabricar (amb merma) = N + 30

Superfície total = (N + 30) × 0,0129375 m²
Pes total = Superfície × 0,070 kg

Cost material = Pes × 9,45 €
Ports proporcionals = 20,00 × (Pes / 51,5)
Cost material total = Cost material + Ports proporcionals

### 5.2 Transformació

Preparació = 0,25 h × 31,70 €

Picades necessàries = (N + 30) / 2
Temps tiratge = Picades / 1.800 hores
Cost tiratge = Temps tiratge × 31,70 €

Desbobinar = (N / 2.000 × 10 / 60) h × 19,93 €

Tallar = (5/60) h × 27,73 €

Destroquelar = ((N + 30) / 1.000 × 5 / 60) h × 19,93 €

Embalatge = (5/60) h × 19,93 €

Total transformació = Suma de tots els conceptes


### 5.3 Generals

Generals = 5,00 + 3,00 = 8,00 €


### 5.4 Cost total i preu de venda

Cost total = Cost material total + Total transformació + Generals
Preu venda (sense IVA) = Cost total × 4 [300% marge]
Preu unitari = Preu venda / N


---

## 6. EXEMPLES DE CÀLCUL

### Exemple 1: 1.000 peces

| Concepte | Càlcul | Import (€) |
| :--- | :--- | :--- |
| Peces amb merma | 1.000 + 30 | 1.030 |
| Superfície total | 1.030 × 0,0129375 | 13,3256 m² |
| Pes total | 13,3256 × 0,070 | 0,9328 kg |
| Cost material | 0,9328 × 9,45 | 8,81 € |
| Ports proporcionals | 20 × (0,9328/51,5) | 0,36 € |
| **Material total** | | **9,17 €** |
| Preparació troqueladora | 0,25 × 31,70 | 7,93 € |
| Tiratge | (1.030/2)/1.800 × 31,70 | 9,07 € |
| Desbobinar | (1.000/2.000×10/60) × 19,93 | 1,66 € |
| Tallar trossos | (5/60) × 27,73 | 2,31 € |
| Destroquelar | (1.030/1.000×5/60) × 19,93 | 1,71 € |
| Embalatge | (5/60) × 19,93 | 1,66 € |
| **Total transformació** | | **24,34 €** |
| Transport + Gestió | | **8,00 €** |
| **COST TOTAL** | | **41,51 €** |
| **Marge (300%)** | | **124,53 €** |
| **PREU VENDA (sense IVA)** | | **166,04 €** |
| **Preu unitari de venda** | | **0,1660 €** |

---

### Exemple 2: 2.500 peces

| Concepte | Import (€) |
| :--- | :--- |
| **Material total (amb merma + ports)** | **21,68 €** |
| Preparació troqueladora | 7,93 € |
| Tiratge | 22,28 € |
| Desbobinar | 4,15 € |
| Tallar trossos | 2,31 € |
| Destroquelar | 4,20 € |
| Embalatge | 1,66 € |
| **Total transformació** | **42,53 €** |
| Transport + Gestió | **8,00 €** |
| **COST TOTAL** | **72,21 €** |
| **Marge (300%)** | **216,63 €** |
| **PREU VENDA (sense IVA)** | **288,84 €** |
| **Preu unitari de venda** | **0,1155 €** |

---

### Exemple 3: 5.000 peces

| Concepte | Import (€) |
| :--- | :--- |
| **Material total (amb merma + ports)** | **42,31 €** |
| Preparació troqueladora | 7,93 € |
| Tiratge | 44,29 € |
| Desbobinar | 8,30 € |
| Tallar trossos | 2,31 € |
| Destroquelar | 8,35 € |
| Embalatge | 1,66 € |
| **Total transformació** | **72,84 €** |
| Transport + Gestió | **8,00 €** |
| **COST TOTAL** | **123,15 €** |
| **Marge (300%)** | **369,45 €** |
| **PREU VENDA (sense IVA)** | **492,60 €** |
| **Preu unitari de venda** | **0,0985 €** |

---

## 7. RESUM COMPARATIU

| Concepte | 1.000 peces | 2.500 peces | 5.000 peces |
| :--- | :--- | :--- | :--- |
| Peces amb merma | 1.030 | 2.530 | 5.030 |
| Superfície total (m²) | 13,33 | 32,73 | 65,08 |
| Pes total (kg) | 0,93 | 2,29 | 4,56 |
| Cost material (amb ports) | 9,17 € | 21,68 € | 42,31 € |
| Total transformació | 24,34 € | 42,53 € | 72,84 € |
| Generals | 8,00 € | 8,00 € | 8,00 € |
| **Cost total** | **41,51 €** | **72,21 €** | **123,15 €** |
| **Marge (300%)** | **124,53 €** | **216,63 €** | **369,45 €** |
| **Preu venda (sense IVA)** | **166,04 €** | **288,84 €** | **492,60 €** |
| **Preu unitari de venda** | **0,1660 €** | **0,1155 €** | **0,0985 €** |

---

## 8. TAULA DE PREUS UNITARIS PER QUANTITAT

| Quantitat | Preu unitari (300% marge) |
| :--- | :--- |
| **1.000** | **0,1660 €** |
| **2.500** | **0,1155 €** |
| **5.000** | **0,0985 €** |

---

## 9. FORMULARI PER A NOVES COMANDES

**Omple les dades següents per calcular una nova comanda:**

| Dada | Valor |
| :--- | :--- |
| Nombre de peces finals (N) | |
| Merma (peces) | 30 |
| Preu material (€/kg) | 9,45 |
| Marge comercial (%) | 300 |
| Costos generals fixos | 8,00 € |

**Resultats:**

| | Import |
| :--- | :--- |
| Material total | |
| Transformació total | |
| Generals | 8,00 € |
| **Cost total** | |
| **Preu venda (sense IVA)** | |
| **Preu unitari** | |

---

## 10. OBSERVACIONS

- La merma s'ha fixat en 30 peces per comanda per ajustos i proves inicials.
- Els ports es calculen de manera proporcional al pes de material utilitzat.
- Els temps de transformació són estàndards; ajustar segons cas real si cal.
- El marge del 300% és sobre el cost total (preu = cost × 4).
- L'IVA no està inclòs en cap dels càlculs.
- El desbobinat es calcula a raó de **10 minuts per cada 2.000 peces finals** (diferència respecte al model de 75 µm).
- El tallar trossos i l'embalatge són costos fixos de 5 minuts per comanda.

---
