# 📦 Procediment de fabricació d'etiquetes adhesives
## (Base per a pressupostos i planificació de comandes)

---

## 1. FULL ESTÀNDARD

- **Mida full:** 320 × 450 mm (SRA3)
- **Vora de seguretat:** 8 mm a cada costat
- **Zona útil:** 304 × 434 mm
- **Tall entre etiquetes:** Únic (no cal doble tall ni canals)

---

## 2. CÀLCUL D'ETIQUETES PER FULL

Per a cada mida d'etiqueta, es calculen les **dues orientacions** i s'escull la que doni més unitats per full.

### Fórmula

etiquetes_ample = part_entera(zona_útil_ample / amplada_etiqueta)
etiquetes_alt = part_entera(zona_útil_alt / altura_etiqueta)
total_per_full = etiquetes_ample × etiquetes_alt

### Exemples

| Mida (mm) | Orientació òptima (ample × alt) | Etq./full |
|-----------|--------------------------------|-----------|
| 40 × 60   | 60 × 40                        | 50        |
| 35 × 45   | 35 × 45 (o 45 × 35)            | 72        |
| 45 × 12   | 12 × 45                        | 225       |
| 80 × 120  | 80 × 120                       | 10        |
| 67 × 60   | 60 × 67                        | 30        |
| 50 × 20   | 50 × 20                        | 126       |
| 30 × 60   | 30 × 60 (o 60 × 30)            | 70        |

---

## 3. MÈTODES DE TALL

### 3.1. Guillotinat (tall complet)
- **Ús:** Etiquetes rectangulars sense mig tall, amb talls al revers o per a ús intern.
- **Temps:** 10 minuts fixos per comanda (independent del nombre de fulls).
- **Cost:** 27,78 €/h.
- **Observació:** Si hi ha diversos models d'una comanda, es reparteix el temps:
  - 1r model: 10 min
  - Models addicionals: 5 min cadascun

### 3.2. Mig tall manual (troquelat amb regle i cúter)
- **Ús:** Etiquetes que s'han de desprendre fàcilment, per a tirades petites.
- **Temps per full:** Segons taula d'escalat (veure punt 4).
- **Cost:** 33 €/h.
- **Proporció de talls:** 2/3 llargs (450 mm) – 1/3 curts (320 mm).
- **Temps estàndard per tall:** 6 segons (tant vertical com horitzontal).
- **Temps de canvi de full i gir de sentit:** 20 segons per full.

### 3.3. Mig tall amb troqueladora Heidelberg d'aspes (full a full)
- **Ús:** Tirades mitjanes i grans d'etiquetes rectangulars, amb necessitat de mig tall.
- **Màquina:** Heidelberg d'aspes (full a full, en pla).
- **Format màxim del full:** 250 × 350 mm.
- **Format promig de treball:** 160 × 225 mm (1/4 de SRA3).
- **Velocitat de treball:** 2.000 fulls/hora (per a format promig).
- **Cost hora màquina:** 31,70 €/h.

#### Procés de treball
- **Dues passades** per full:
  1. **1a passada:** Talls en sentit horitzontal (llarg del full)
  2. **2a passada:** Talls en sentit vertical (ample del full)
- **Motiu:** Més pràctic que muntar un motlle amb els dos sentits de cop (evita tallar flejes a mida i col·locar peces d'imposició).

#### Temps de preparació (setup)
- **1a passada (horitzontal):** 15 minuts
- **2a passada (vertical):** 10 minuts
- **Total preparació per comanda:** 25 minuts

#### Observació important
- El full que surt de la impressora (SRA3) **NO** és el mateix que entra a la troqueladora.
- Cal preguntar sempre la **mida de troquelat** (format que admet la Heidelberg).
- Normalment, el SRA3 (320×450 mm) es divideix en **4 parts** de 160×225 mm per entrar a la màquina.

#### Fórmula de càlcul (Heidelberg)

1. Etiquetes per full SRA3 (impressió)

2. Fulls SRA3 = sostre(etiquetes_totals / etiquetes_per_full_SRA3)

3. Subfulls Heidelberg = Fulls SRA3 × 4 (si es divideix en 4 parts)

4. Passades totals = Subfulls Heidelberg × 2 (dues passades per full)

5. Temps troquelat (h) = Passades totals / 2000 fulls/h

6. Temps preparació (h) = 25 min / 60 = 0,4167 h

7. Temps total (h) = Temps troquelat + Temps preparació

8. Cost troquelat = Temps total × 31,70 €/h


#### Exemple pràctic
**Comanda:** 1.000 etiquetes de 25 × 60 mm

| Pas | Concepte | Càlcul | Resultat |
|-----|----------|--------|----------|
| 1 | Etq./full SRA3 | 304÷25=12, 434÷60=7 → 12×7 | 84 |
| 2 | Fulls SRA3 | 1000÷84=11,9 → | 12 fulls |
| 3 | Subfulls Heidelberg | 12 × 4 | 48 subfulls |
| 4 | Passades totals | 48 × 2 | 96 passades |
| 5 | Temps troquelat | 96 ÷ 2000 | 0,048 h (2,88 min) |
| 6 | Temps preparació | 25 min | 0,4167 h |
| 7 | Temps total | 0,048 + 0,4167 | 0,4647 h |
| 8 | Cost troquelat | 0,4647 × 31,70 € | **14,73 €** |

---

## 4. TAULA D'ESCALAT PER A MIG TALL MANUAL

| Etq./full | Temps total (min) | Cost/full (33 €/h) |
|-----------|-------------------|--------------------|
| 25        | 1,133             | 0,623 €            |
| 50        | 1,633             | 0,898 €            |
| 75        | 2,033             | 1,118 €            |
| 100       | 2,233             | 1,228 €            |
| 125       | 2,533             | 1,393 €            |
| 150       | 2,833             | 1,558 €            |
| 175       | 3,033             | 1,668 €            |
| 200       | 3,333             | 1,833 €            |
| **250**   | **4,233**         | **2,328 €**        |
| 300       | 4,333             | 2,383 €            |
| 400       | 5,333             | 2,933 €            |
| 500       | 6,333             | 3,483 €            |
| 750       | 8,833             | 4,858 €            |
| 1000      | 11,333            | 6,233 €            |

**Nota:** Si el nombre d'etiquetes per full no està a la taula, s'usa el **valor immediatament superior**.

---

## 5. ESTRUCTURA DE COSTOS

| Partida                       | Càlcul / Base                                  |
|-------------------------------|------------------------------------------------|
| **Material**                  | €/full × nombre de fulls                       |
| **Impressió**                 | €/click × nombre de fulls × factor de volum    |
| **Preimpressió**              | 15 min base (33 €/h) + 5 min/model addicional  |
| **Tall**                      | Guillotinat / Mig tall manual / Heidelberg     |
| **Empaquetat + transport**    | 6 € base + 1,5 min per model (19,93 €/h)       |

### Factors de correcció d'impressió (click color)

| Volum / Situació         | Factor aplicat |
|--------------------------|----------------|
| Baix volum (≤ 30 fulls)  | ×10            |
| Volum mitjà              | ×4 o ×6 (segons criteri) |
| Alt volum (> 500 fulls)  | ×1 (estàndard) |

---

## 6. EXEMPLES PRÀCTICS

### Exemple 1: 800 etiquetes (45×12 mm), mig tall manual, 225/full

| Partida           | Càlcul                     | Import |
|-------------------|----------------------------|--------|
| Material          | 4 fulls × 0,28 €           | 1,12 € |
| Impressió         | 4 × 0,06 €                 | 0,24 € |
| Preimpressió      | 15 min (33 €/h)            | 8,25 € |
| Mig tall manual   | 4 fulls × 2,328 € (taula 250) | 9,31 € |
| Empaq.+transp.    | Fix                        | 6,00 € |
| **TOTAL**         |                            | **24,92 €** |

---

### Exemple 2: 450 etiquetes (80×120 mm), guillotinat, estucat brillant, click ×6

| Partida           | Càlcul                         | Import |
|-------------------|--------------------------------|--------|
| Material          | 45 fulls × 0,2553 €            | 11,49 € |
| Impressió (×6)    | 45 × 0,317778 €                | 14,30 € |
| Preimpressió      | 15 min                         | 8,25 € |
| Guillotinat       | 10 min                         | 4,63 € |
| Empaq.+transp.    | Fix                            | 6,00 € |
| **COST BASE**     |                                | **44,67 €** |
| Marge 50%         |                                | 22,34 € |
| **PREU VENDA**    |                                | **67,01 €** |

---

### Exemple 3: 1.000 etiquetes (25×60 mm), mig tall Heidelberg, SRA3, 84/full

| Partida               | Càlcul                         | Import |
|-----------------------|--------------------------------|--------|
| Material              | 12 fulls × 0,28 € (òfset)       | 3,36 € |
| Impressió             | 12 × 0,06 €                    | 0,72 € |
| Preimpressió          | 15 min (33 €/h)                | 8,25 € |
| Mig tall Heidelberg   | (veure càlcul pas a pas)       | 14,73 € |
| Empaq.+transp.        | Fix                            | 6,00 € |
| **TOTAL**             |                                | **33,06 €** |
| **€/etiqueta**        | 33,06 ÷ 1000                   | **0,033 €** |

---

## 7. MATERIALS DISPONIBLES (preus / full SRA3)

| Material                     | Preu / full |
|------------------------------|-------------|
| Adhesiu òfset                | 0,1915 €    |
| Adhesiu estucat brillant     | 0,2553 €    |

---

## 8. NOTES PER A FUTURES COMANDES

- **Sempre** calcular les dues orientacions de l'etiqueta.
- Per a **mig tall manual**, usar la taula d'escalat.
- Per a **guillotinat**, temps fix de 10 min (més 5 min per model addicional).
- Per a **mig tall amb Heidelberg d'aspes**:
  - Preguntar sempre la mida de troquelat (subfull).
  - SRA3 normalment es divideix en 4 parts.
  - Dues passades per full (horitzontal + vertical).
  - Preparació: 15 + 10 minuts.
  - Velocitat: 2.000 fulls/hora.
  - Cost: 31,70 €/h.
- El factor d'impressió s'aplica segons volum i criteri de rendibilitat.
- Guardar aquest document com a referència per a futures consultes.

---

> 📌 **Versió:** 2.1  
> 📅 **Data:** 2026-08-25  
> ✏️ **Elaborat a partir de dades reals de producció**  
> 🔄 **Actualització:** Corregit cost hora d'embalatge a 19,93 €
