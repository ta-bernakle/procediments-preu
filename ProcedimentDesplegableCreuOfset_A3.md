# PROCEDIMENT ESTÀNDARD: DESPLEGABLES OFFSET (GRANS TIRADES)
**Versió:** 1.0  
**Data:** 2026-07-03  
**Tipus:** Offset, quadricromia, plegat en creu  
**Àmbit:** Tirades grans (≥ 1.000 unitats)  

---

## 1. DESCRIPCIÓ DEL PRODUCTE

| Concepte | Descripció |
|----------|------------|
| **Producte** | Desplegable (díptic, tríptic, plegat en creu, etc.) |
| **Impressió** | Offset, color (quadricromia: CMYK), 2 cares |
| **Paper** | Òfset 90 g (o gramatge similar) |
| **Format màquina** | 450 × 640 mm (o similar) |
| **Acabats** | Guillotinat + plegat (una o dues passades) |

---

## 2. PARÀMETRES FIXOS

### 2.1. Paper
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Format màquina | 450 × 640 | mm |
| Superfície | 0,288 | m² |
| Gramatge (per defecte) | 90 | g/m² |
| Preu per kg (per defecte) | 1,45 | €/kg |
| Cost per full | 0,037584 | €/full |

**Fórmula:**  
`Cost_full = (0,45 × 0,64) × (gramatge_kg) × preu_kg`

### 2.2. Planxes
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Cost per planxa | 21,00 | € |
| Planxes necessàries | 4 (CMYK) | unitats |
| Cost total planxes | 84,00 | € |

### 2.3. Muntatge de planxes
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps de muntatge | 105 | minuts |
| Cost hora | 87,88 | €/h |
| Cost muntatge | 153,79 | € |

### 2.4. Impressió
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Passades per cara | 2 | passades |
| Passades totals (2 cares) | 4 | passades |
| Velocitat | 6.000 | fulls/hora |
| Cost hora | 87,88 | €/h |

### 2.5. Preparació document (imposició)
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps | 20 | minuts |
| Cost hora | 33,08 | €/h |
| Cost preparació | 11,03 | € |

### 2.6. Guillotinat
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps (per defecte) | 0,75 | hores |
| Cost hora | 27,78 | €/h |

### 2.7. Plegat
| Paràmetre | 1a passada | 2a passada | Unitat |
|-----------|------------|------------|--------|
| Temps base | 56 | 56 × 1,3 = 72,8 | minuts |
| Increment de temps | — | +30% | — |
| Cost hora | 39,65 | 39,65 | €/h |

### 2.8. Embalatge
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Capacitat per caixa | 2.000 | unitats |
| Cost per caixa | 1,60 | € |
| Temps d'embalatge | 30 | minuts |
| Cost hora | 19,93 | €/h |

### 2.9. Transport
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Cost fix per comanda | 5,00 | € |

### 2.10. Maculatura
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Fulls de prova (per defecte) | 200 | fulls 450×640 |
| Unitats equivalents | 400 | unitats |

---

## 3. FÓRMULES

### 3.1. Càlcul de fulls i impressions

Unitats_producció = Unitats_client + Maculatura_unitats
Fulls_màquina = CEILING(Unitats_producció / Unitats_per_full)
Impressions_totals = Fulls_màquina × Passades_totals


### 3.2. Cost paper

Cost_paper = Fulls_màquina × Cost_per_full


### 3.3. Cost impressió

Temps_impressió = (Fulls_màquina / Velocitat) × Passades_totals
Cost_impressió = Temps_impressió × Cost_hora_impressió


### 3.4. Cost plegat

Temps_plegat = (Temps_1a_passada / 60) + (Temps_2a_passada / 60)
Cost_plegat = Temps_plegat × Cost_hora_plegat


### 3.5. Cost embalatge

Caixes = CEILING(Unitats_client / Capacitat_caixa)
Cost_embalatge = (Caixes × Cost_caixa) + (Temps_embalatge / 60 × Cost_hora_embalatge)


### 3.6. Cost total

COST_NET = Cost_paper + Cost_planxes + Cost_muntatge + Cost_impressió + Cost_preparació + Cost_guillotinat + Cost_plegat + Cost_embalatge + Cost_transport


### 3.7. Preu de venda

PREU_VENDA = COST_NET × (1 + Marge_%)
Preu_unitari = PREU_VENDA / Unitats_client


---

## 4. EXEMPLE D'APLICACIÓ

### Dades d'entrada
| Paràmetre | Valor |
|-----------|-------|
| Unitats client | 6.500 |
| Maculatura | 200 fulls |
| Marge | 30% |

### Resultats
| Concepte | Import |
|----------|--------|
| Paper | 129,66 € |
| Planxes | 84,00 € |
| Muntatge planxes | 153,79 € |
| Impressió | 202,12 € |
| Preparació | 11,03 € |
| Guillotinat | 20,84 € |
| Plegat | 85,10 € |
| Embalatge | 16,37 € |
| Transport | 5,00 € |
| **COST NET** | **707,91 €** |
| **PREU VENDA (30%)** | **920,28 €** |
| **Preu unitari** | **0,1416 €** |

---

## 5. NOTES PER A FUTURES ADAPTACIONS

| Situació | Acció |
|----------|-------|
| Canvi de gramatge | Actualitzar `gramatge_kg` i `preu_kg` |
| Canvi de nombre de plecs | Ajustar `Temps_1a_passada` i `Temps_2a_passada` |
| Canvi de format de màquina | Actualitzar `Format_màquina` i `Unitats_per_full` |
| Impressió a 1 cara | Reduir `Passades_totals` a 2 |
| Marge diferent | Canviar `Marge_%` |

---

## 6. VERSIONS

| Versió | Data | Canvis |
|--------|------|--------|
| 1.0 | 2026-07-03 | Creació inicial del procediment |

---

**FI DEL DOCUMENT**
