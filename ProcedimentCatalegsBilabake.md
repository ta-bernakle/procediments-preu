# PROCEDIMENT ESTÀNDARD: CATÀLEGS BILABAKE
**Versió:** 1.0  
**Data:** 2026-07-20  
**Tipus:** Digital (Versant 4100), color 1 cara, SRA3  
**Àmbit:** Tirades petites (≤ 1000 impressions)  

---

## 1. DESCRIPCIÓ DEL PRODUCTE

| Concepte | Descripció |
|----------|------------|
| **Producte** | Catàleg en fulls solts DIN A-4 (color, una cara) |
| **Material interior** | Òfset 100 g |
| **Material portada/contraportada** | Estucat 250 g |
| **Impressió** | Digital (Versant 4100), color, 1 cara |
| **Format màquina** | SRA3 (320 × 450 mm) |
| **Rendiment** | 2 unitats DIN A-4 per full SRA3 |
| **Acabats** | Guillotinat (per separat) |

---

## 2. PARÀMETRES FIXOS

### 2.1. Impressió (digital)
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Cost click color SRA3 (base) | 0,059 | €/cara |
| Factor multiplicador (segons volum) | Veure taula 2.1.1 | — |

#### Taula 2.1.1: Factor multiplicador per volum d'impressions
| Volum (impressions) | Factor multiplicador |
|---------------------|----------------------|
| Fins a 250 | 8× |
| De 251 a 500 | 6× |
| De 501 a 1.000 | 4× |

---

### 2.2. Paper interior (òfset 100 g)
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Format SRA3 | 320 × 450 | mm |
| Superfície | 0,144 | m² |
| Gramatge | 100 | g/m² |
| Preu per kg | 1,45 | €/kg |
| **Cost per full SRA3** | **0,02088** | €/full |

**Fórmula:**  
`Cost_full_interior = 0,144 × 0,100 × 1,45 = 0,02088 €`

---

### 2.3. Paper portada/contraportada (estucat 250 g)
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Format SRA3 | 320 × 450 | mm |
| Superfície | 0,144 | m² |
| Gramatge | 250 | g/m² |
| Preu per kg | 2,90 | €/kg |
| **Cost per full SRA3** | **0,1044** | €/full |

**Fórmula:**  
`Cost_full_portada = 0,144 × 0,250 × 2,90 = 0,1044 €`

---

### 2.4. Maculatura
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Fulls SRA3 de prova (interior) | 6 | fulls |
| Fulls SRA3 de prova (portada) | 0 | fulls |

---

### 2.5. Costos fixos (per treball)
| Concepte | Temps | Cost hora | Cost fix |
|----------|-------|-----------|----------|
| Preparació / imposició | 15 min | 33,08 €/h | 8,27 € |
| Guillotinat | 10 min | 27,78 €/h | 4,63 € |
| Embalatge | 5 min | 19,93 €/h | 1,66 € |
| Transport | — | — | 5,00 € |

---

### 2.6. Marge comercial
| Paràmetre | Valor |
|-----------|-------|
| Marge per defecte | 50% |

---

## 3. ENTRADA DE DADES (per a cada treball)

| Dada | Exemple |
|------|---------|
| Models (quantitat) | 3 |
| Per a cada model: pàgines interiors | 4, 6, 8 |
| Per a cada model: unitats | 50, 30, 20 |
| Portada i contraportada? | Sí / No |

---

## 4. FÓRMULES DE CÀLCUL

### 4.1. Càlcul d'unitats totals
Unitats_interior = SUMA(Unitats_model_i)

text

### 4.2. Càlcul de pàgines totals i impressions
Pàgines_totals_interior = SUMA(Unitats_model_i × Pàgines_model_i)
Impressions_interior = Pàgines_totals_interior (perquè és 1 cara)

text

### 4.3. Càlcul de fulls SRA3 (interior)
Fulls_SRA3_interior_net = CEILING(Impressions_interior / 2)
Fulls_SRA3_interior_producció = Fulls_SRA3_interior_net + Maculatura_interior (6 fulls)

text

### 4.4. Càlcul de portada (si n'hi ha)
Impressions_portada = Unitats_interior × 2 (1 portada + 1 contraportada per unitat)
Fulls_SRA3_portada = CEILING(Impressions_portada / 2)

text
*(No s'aplica maculatura a la portada)*

### 4.5. Càlcul de cost paper
Cost_paper_interior = Fulls_SRA3_interior_producció × 0,02088
Cost_paper_portada = Fulls_SRA3_portada × 0,1044

text

### 4.6. Càlcul total d'impressions (per factor multiplicador)
Impressions_totals = Impressions_interior + Impressions_portada
Factor_multiplicador = Segons taula 2.1.1
Cost_click_efectiu = 0,059 × Factor_multiplicador

text

### 4.7. Càlcul cost impressió
Cost_impressió = Impressions_totals × 0,059 × Factor_multiplicador

text

### 4.8. Càlcul cost total
COST_NET = Cost_impressió + Cost_paper_interior + Cost_paper_portada + 8,27 + 4,63 + 1,66 + 5,00

text

### 4.9. Preu de venda
PREU_VENDA = COST_NET × (1 + Marge_%)
Preu_unitari = PREU_VENDA / Unitats_interior

text

---

## 5. EXEMPLE D'APLICACIÓ

### Dades d'entrada
| Model | Pàgines | Unitats | Impressions (pàgines × unitats) |
|-------|---------|---------|--------------------------------|
| A | 4 | 50 | 200 |
| B | 6 | 30 | 180 |
| C | 8 | 20 | 160 |
| **Total interior** | — | 100 | **540** |
| Portada | — | — | 200 (100 × 2) |
| **Total impressions** | — | — | **740** |

### Resultats
| Concepte | Càlcul | Import |
|----------|--------|--------|
| Paper interior | (540/2 + 6) × 0,02088 | 5,76 € |
| Paper portada | (200/2) × 0,1044 | 10,44 € |
| Impressions | 740 × 0,059 × 4 | 174,64 € |
| Preparació | 8,27 | 8,27 € |
| Guillotinat | 4,63 | 4,63 € |
| Embalatge | 1,66 | 1,66 € |
| Transport | 5,00 | 5,00 € |
| **COST NET** | | **210,40 €** |
| **PREU VENDA (50%)** | | **315,60 €** |
| **Preu unitari** | 315,60 / 100 | **3,156 €/catàleg** |

---

## 6. NOTES PER A FUTURES ADAPTACIONS

| Situació | Acció |
|----------|-------|
| Sense portada | Eliminar `Cost_paper_portada` i `Impressions_portada` |
| Canvi de gramatge | Actualitzar `gramatge_kg` i `preu_kg` |
| Canvi de format de màquina | Actualitzar `format_màquina` i `unitats_per_full` |
| Impressió a 2 cares | Multiplicar `Impressions_totals` per 2 |
| Marge diferent | Canviar `Marge_%` |

---

## 7. VERSIONS

| Versió | Data | Canvis |
|--------|------|--------|
| 1.0 | 2026-07-20 | Creació inicial del procediment |

---

**FI DEL DOCUMENT**
