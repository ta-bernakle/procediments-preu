PROCEDIMENT: IMPRESSIÓ SOBRE MATERIAL DEL CLIENT (VERSANT 4100)
markdown
# PROCEDIMENT ESTÀNDARD: IMPRESSIÓ SOBRE MATERIAL DEL CLIENT (SRA3)
**Versió:** 1.0  
**Data:** 2026-07-08  
**Tipus:** Impressió digital (Versant 4100) sobre SRA3 (material del client)  
**Àmbit:** Tirades petites/mitjanes (≤ 500 unitats)  

---

## 1. DESCRIPCIÓ DEL PRODUCTE

| Concepte | Descripció |
|----------|------------|
| **Producte** | Impressió en "rama" (plec de fulls SRA3, sense tall posterior) |
| **Material** | Subministrat pel client (paper SRA3) |
| **Impressió** | Digital (Versant 4100), color, una o dues cares (preguntar) |
| **Acabats** | Guillotinat previ (formatar material 700×1000 → SRA3) + embalatge |
| **Preparació** | Gestió de comanda + preparació del fitxer digital |

---

## 2. PARÀMETRES FIXOS

### 2.1. Impressió
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Cost click color SRA3 (base) | 0,059 | €/cara |
| Factor multiplicador per defecte | 8 | — |
| Cost click efectiu | 0,472 | €/cara |

### 2.2. Preparació i gestió
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps | 15 | minuts |
| Cost hora | 33,08 | €/h |
| Cost fix | 8,27 | € |

### 2.3. Guillotinat previ (formatar material)
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps mínim | 10 | minuts |
| Cost hora | 27,78 | €/h |
| Cost fix | 4,63 | € |

### 2.4. Embalatge
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Temps | 5 | minuts |
| Cost hora | 19,93 | €/h |
| Cost fix | 1,66 | € |

### 2.5. Transport
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Cost fix | 5,00 | € |

### 2.6. Maculatura
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Fulls SRA3 extra | 6 | fulls |
| Impressions de maculatura | Sí (es comptabilitzen) | — |

### 2.7. Marge comercial
| Paràmetre | Valor | Unitat |
|-----------|-------|--------|
| Marge per defecte | 50% | — |

---

## 3. FÓRMULES

### 3.1. Càlcul de fulls i impressions
Unitats_producció = Unitats_client + Maculatura
Impressions = Unitats_producció × cares_per_full

text

### 3.2. Cost impressió
Cost_impressió = Impressions × 0,059 × factor_multiplicador

text

### 3.3. Cost total
COST_NET = Cost_impressió + 8,27 + 4,63 + 1,66 + 5,00

text

### 3.4. Preu de venda
PREU_VENDA = COST_NET × (1 + Marge_%)

text

---

## 4. EXEMPLE D'APLICACIÓ (150 unitats, 1 cara)

### Dades d'entrada
| Paràmetre | Valor |
|-----------|-------|
| Unitats client | 150 |
| Maculatura | 6 |
| Unitats producció | 156 |
| Impressions | 156 |
| Factor multiplicador | 8 |
| Marge | 50% |

### Resultats
| Concepte | Import |
|----------|--------|
| Impressió (156 × 0,059 × 8) | 73,63 € |
| Preparació/gestió | 8,27 € |
| Guillotinat previ | 4,63 € |
| Embalatge | 1,66 € |
| Transport | 5,00 € |
| **COST NET** | **93,19 €** |
| **PREU VENDA (50%)** | **139,79 €** |

---

## 5. NOTES PER A FUTURES ADAPTACIONS

| Situació | Acció |
|----------|-------|
| Impressió a 2 cares | Multiplicar Impressions per 2 |
| Factor multiplicador diferent | Substituir el 8 pel valor indicat pel client |
| Marge diferent | Canviar `Marge_%` |
| Tirada més gran | Mantenir costos fixos (preparació, guillotinat, embalatge) |
| Material diferent (no SRA3) | Ajustar procés de guillotinat si cal |
| Sense guillotinat previ | Eliminar cost de guillotinat (4,63 €) |

---

## 6. PREGUNTES OBLIGATÒRIES PER A CADA FEINA

- **Impressió a una o dues cares?**
- **Quina quantitat d'unitats vol el client?**
- **Factor multiplicador del click?** (per defecte: 8)
- **Marge comercial?** (per defecte: 50%)

---

## 7. VERSIONS

| Versió | Data | Canvis |
|--------|------|--------|
| 1.0 | 2026-07-08 | Creació inicial del procediment |

---

**FI DEL DOCUMENT**
