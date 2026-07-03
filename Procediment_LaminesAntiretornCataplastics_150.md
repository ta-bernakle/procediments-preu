# PROCEDIMENT ESTÀNDARD: CÀLCUL DE COSTOS DE PEÇES TROQUELADES
## Film de polièster - 75 µm (Peces grans)
### Marge comercial: 300% (preu = cost × 4)

---

## 1. DADES FIXES DEL MATERIAL

| Paràmetre | Valor | Unitat |
| :--- | :--- | :--- |
| Material | Film polièster 75 µm | - |
| Gramatge | 105 | g/m² |
| Densitat | 1.400 | kg/m³ |
| Rendiment | 9,5238 | m²/kg |
| Preu material | 9,45 | €/kg |
| Pes bobina sencera | 51,5 | kg |
| Cost ports per bobina | 20,00 | € |
| Amplada bobina | 500 | mm |
| Longitud de llesca (desenvolupament) | 330 | mm |
| Mida peça final | 167 × 165 | mm |
| Mida format (peça doble) | 330 × 166,66 | mm |
| Peces finals per llesca | 6 | unitats |
| Superfície per llesca | 0,1650 | m² |
| Superfície per peça final | 0,027555 | m² |
| Pes per peça final | 0,002893275 | kg |

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
| Temps desbobinar | 5 min / 2.000 peces |

---

## 5. PROCEDIMENT DE CÀLCUL PER A `N` PEÇES FINALS

### 5.1 Material

Peces totals a fabricar (amb merma) = N + 30

Superfície total = (N + 30) × 0,027555 m²
Pes total = Superfície × 0,105 kg

Cost material = Pes × 9,45 €
Ports proporcionals = 20,00 × (Pes / 51,5)
Cost material total = Cost material + Ports proporcionals


### 5.2 Transformació

Preparació = 0,25 h × 31,70 €

Picades necessàries = (N + 30) / 2
Temps tiratge = Picades / 1.800 hores
Cost tiratge = Temps tiratge × 31,70 €

Desbobinar = (N / 2.000 × 5 / 60) h × 19,93 €

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
| Superfície total | 1.030 × 0,027555 | 28,3817 m² |
| Pes total | 28,3817 × 0,105 | 2,9801 kg |
| Cost material | 2,9801 × 9,45 | 28,16 € |
| Ports proporcionals | 20 × (2,9801/51,5) | 1,16 € |
| **Material total** | | **29,32 €** |
| Preparació troqueladora | 0,25 × 31,70 | 7,93 € |
| Tiratge | (1.030/2)/1.800 × 31,70 | 9,07 € |
| Desbobinar | (1.000/2.000×5/60) × 19,93 | 0,83 € |
| Tallar trossos | (5/60) × 27,73 | 2,31 € |
| Destroquelar | (1.030/1.000×5/60) × 19,93 | 1,71 € |
| Embalatge | (5/60) × 19,93 | 1,66 € |
| **Total transformació** | | **23,51 €** |
| Transport + Gestió | | **8,00 €** |
| **COST TOTAL** | | **60,83 €** |
| **Marge (300%)** | | **182,49 €** |
| **PREU VENDA (sense IVA)** | | **243,32 €** |
| **Preu unitari de venda** | | **0,2433 €** |

---

### Exemple 2: 2.500 peces

| Concepte | Import (€) |
| :--- | :--- |
| **Material total (amb merma + ports)** | **72,01 €** |
| Preparació troqueladora | 7,93 € |
| Tiratge | 22,28 € |
| Desbobinar | 2,08 € |
| Tallar trossos | 2,31 € |
| Destroquelar | 4,20 € |
| Embalatge | 1,66 € |
| **Total transformació** | **40,45 €** |
| Transport + Gestió | **8,00 €** |
| **COST TOTAL** | **120,46 €** |
| **Marge (300%)** | **361,38 €** |
| **PREU VENDA (sense IVA)** | **481,84 €** |
| **Preu unitari de venda** | **0,1927 €** |

---

### Exemple 3: 5.000 peces

| Concepte | Import (€) |
| :--- | :--- |
| **Material total (amb merma + ports)** | **143,18 €** |
| Preparació troqueladora | 7,93 € |
| Tiratge | 44,29 € |
| Desbobinar | 4,15 € |
| Tallar trossos | 2,31 € |
| Destroquelar | 8,35 € |
| Embalatge | 1,66 € |
| **Total transformació** | **68,70 €** |
| Transport + Gestió | **8,00 €** |
| **COST TOTAL** | **219,88 €** |
| **Marge (300%)** | **659,64 €** |
| **PREU VENDA (sense IVA)** | **879,52 €** |
| **Preu unitari de venda** | **0,1759 €** |

---

## 7. RESUM COMPARATIU

| Concepte | 1.000 peces | 2.500 peces | 5.000 peces |
| :--- | :--- | :--- | :--- |
| Peces amb merma | 1.030 | 2.530 | 5.030 |
| Superfície total (m²) | 28,38 | 69,71 | 138,60 |
| Pes total (kg) | 2,98 | 7,32 | 14,55 |
| Cost material (amb ports) | 29,32 € | 72,01 € | 143,18 € |
| Total transformació | 23,51 € | 40,45 € | 68,70 € |
| Generals | 8,00 € | 8,00 € | 8,00 € |
| **Cost total** | **60,83 €** | **120,46 €** | **219,88 €** |
| **Marge (300%)** | **182,49 €** | **361,38 €** | **659,64 €** |
| **Preu venda (sense IVA)** | **243,32 €** | **481,84 €** | **879,52 €** |
| **Preu unitari de venda** | **0,2433 €** | **0,1927 €** | **0,1759 €** |

---

## 8. TAULA DE PREUS UNITARIS PER QUANTITAT

| Quantitat | Preu unitari (300% marge) |
| :--- | :--- |
| **1.000** | **0,2433 €** |
| **2.500** | **0,1927 €** |
| **5.000** | **0,1759 €** |

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
- El desbobinat es calcula a raó de **5 minuts per cada 2.000 peces finals**.
- El tallar trossos i l'embalatge són costos fixos de 5 minuts per comanda.

---
