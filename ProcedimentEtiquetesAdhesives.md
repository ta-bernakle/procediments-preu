# 

# 📦 Procediment de fabricació d'etiquetes adhesives

## (Base per a pressupostos i planificació de comandes)

---

> ⚠️ **NOTA IMPORTANT SOBRE EL MARGE:** El cost de producció calculat en aquest procediment NO inclou costos indirectes (lloguer, assegurances, sou, amortització, màrqueting, impostos, imprevistos). El marge comercial s'aplica sobre el cost de producció i ha de cobrir aquests costos indirectes a més del benefici net. Es recomana revisar el marge segons el volum de la comanda (100-150% per a comandes petites, 75-100% per a mitjanes, 50-75% per a grans, 25-50% per a molt grans) o bé usar marge sobre preu de venda en lloc de marge sobre cost.

---

## 1\. FULL ESTÀNDARD

-   **Mida full:** 320 × 450 mm (SRA3)
    
-   **Vora de seguretat:** 8 mm a cada costat
    
-   **Zona útil:** 304 × 434 mm
    
-   **Tall entre etiquetes:** Únic (no cal doble tall ni canals)
    

---

## 2\. CÀLCUL D'ETIQUETES PER FULL

Per a cada mida d'etiqueta, es calculen les **dues orientacions** i s'escull la que doni més unitats per full.

### Fórmula

etiquetes\_ample = part\_entera(zona\_útil\_ample / amplada\_etiqueta)
etiquetes\_alt = part\_entera(zona\_útil\_alt / altura\_etiqueta)
total\_per\_full = etiquetes\_ample × etiquetes\_alt

### Exemples

| Mida (mm) | Orientació òptima (ample × alt) | Etq./full |
| --- | --- | --- |
| 40 × 60 | 60 × 40 | 50 |
| 35 × 45 | 35 × 45 (o 45 × 35) | 72 |
| 45 × 12 | 12 × 45 | 225 |
| 80 × 120 | 80 × 120 | 10 |
| 67 × 60 | 60 × 67 | 30 |
| 50 × 20 | 50 × 20 | 126 |
| 30 × 60 | 30 × 60 (o 60 × 30) | 70 |

---

## 3\. MÈTODES DE TALL

### 3.1. Guillotinat (tall complet)

-   **Ús:** Etiquetes rectangulars sense mig tall, amb talls al revers o per a ús intern.
    
-   **Temps:** 10 minuts fixos per comanda (independent del nombre de fulls).
    
-   **Cost:** 27,78 €/h.
    
-   **Observació:** Si hi ha diversos models d'una comanda, es reparteix el temps:
    
    -   1r model: 10 min
        
    -   Models addicionals: 5 min cadascun
        

### 3.2. Mig tall manual (troquelat amb regle i cúter)

-   **Ús:** Etiquetes que s'han de desprendre fàcilment, per a tirades petites.
    
-   **Temps per full:** Segons taula d'escalat (veure punt 4).
    
-   **Cost:** 33 €/h.
    
-   **Proporció de talls:** 2/3 llargs (450 mm) – 1/3 curts (320 mm).
    
-   **Temps estàndard per tall:** 6 segons (tant vertical com horitzontal).
    
-   **Temps de canvi de full i gir de sentit:** 20 segons per full.
    

### 3.3. Mig tall amb troqueladora Heidelberg d'aspes (full a full)

-   **Ús:** Tirades mitjanes i grans d'etiquetes rectangulars, amb necessitat de mig tall.
    
-   **Màquina:** Heidelberg d'aspes (full a full, en pla).
    
-   **Format màxim del full:** 250 × 350 mm.
    
-   **Format promig de treball:** 160 × 225 mm (1/4 de SRA3).
    
-   **Velocitat de treball:** 2.000 fulls/hora (per a format promig).
    
-   **Cost hora màquina:** 31,70 €/h.
    

#### Procés de treball

-   **Dues passades** per full:
    
    1.  **1a passada:** Talls en sentit horitzontal (llarg del full)
        
    2.  **2a passada:** Talls en sentit vertical (ample del full)
        
-   **Motiu:** Més pràctic que muntar un motlle amb els dos sentits de cop (evita tallar flejes a mida i col·locar peces d'imposició).
    

#### Temps de preparació (setup)

-   **1a passada (horitzontal):** 15 minuts
    
-   **2a passada (vertical):** 10 minuts
    
-   **Total preparació per comanda:** 25 minuts
    

#### Observació important

-   El full que surt de la impressora (SRA3) **NO** és el mateix que entra a la troqueladora.
    
-   Cal preguntar sempre la **mida de troquelat** (format que admet la Heidelberg).
    
-   Normalment, el SRA3 (320×450 mm) es divideix en **4 parts** de 160×225 mm per entrar a la màquina.
    

#### Fórmula de càlcul (Heidelberg)

1.  Etiquetes per full SRA3 (impressió)
    
2.  Fulls SRA3 = sostre(etiquetes\_totals / etiquetes\_per\_full\_SRA3)
    
3.  Subfulls Heidelberg = Fulls SRA3 × 4 (si es divideix en 4 parts)
    
4.  Passades totals = Subfulls Heidelberg × 2 (dues passades per full)
    
5.  Temps troquelat (h) = Passades totals / 2000 fulls/h
    
6.  Temps preparació (h) = 25 min / 60 = 0,4167 h
    
7.  Temps total (h) = Temps troquelat + Temps preparació
    
8.  Cost troquelat = Temps total × 31,70 €/h
    

#### Exemple pràctic

**Comanda:** 1.000 etiquetes de 25 × 60 mm

| Pas | Concepte | Càlcul | Resultat |
| --- | --- | --- | --- |
| 1 | Etq./full SRA3 | 304÷25=12, 434÷60=7 → 12×7 | 84 |
| 2 | Fulls SRA3 | 1000÷84=11,9 → | 12 fulls |
| 3 | Subfulls Heidelberg | 12 × 4 | 48 subfulls |
| 4 | Passades totals | 48 × 2 | 96 passades |
| 5 | Temps troquelat | 96 ÷ 2000 | 0,048 h (2,88 min) |
| 6 | Temps preparació | 25 min | 0,4167 h |
| 7 | Temps total | 0,048 + 0,4167 | 0,4647 h |
| 8 | Cost troquelat | 0,4647 × 31,70 € | **14,73 €** |

### 3.4. Mig tall amb troqueladora Heidelberg d'aspes amb encuny personalitzat (passada única)

-   **Ús:** Tirades mitjanes i grans d'etiquetes rectangulars, amb necessitat de mig tall, quan es vol **una sola passada per troqueladora** i evitar les dues passades del mètode 3.3.
    
-   **Màquina:** Heidelberg d'aspes (full a full, en pla).
    
-   **Format màxim del full:** 250 × 350 mm.
    
-   **Velocitat de treball:** **1.500 fulls/hora** (a mida màxima 350 × 250 mm, passada única).
    
-   **Cost hora màquina:** 31,70 €/h.
    

#### Procés de treball

-   **Una sola passada per full:** l'encuny ja porta **tots els talls possibles d'un sol cop** (no cal fer horitzontal + vertical per separat).
    
-   El full que entra a la troqueladora és el **subfull de troquelat** (normalment 1/4 de SRA3 = 160 × 225 mm, o la mida que admeti la màquina fins a 250 × 350 mm).
    

#### ⚠️ Pregunta prèvia obligatòria: cost de l'encuny

**Abans de continuar amb el càlcul, cal preguntar si l'encuny personalitzat té cap cost associat** (a part dels processos que implica la feina). Cal distingir:

-   **Encuny ja existent** (reutilitzable d'una comanda anterior): cost d'utillatge = **0 €** (només s'imputa el temps de muntatge/setup).
    
-   **Encuny nou a fabricar per a aquesta comanda:** cal **demanar el pressupost del troquel/encuny** i afegir-lo com a partida pròpia al pressupost (no es pot estimar amb els costos hora d'aquest procediment, ja que depèn del proveïdor d'utillatge).
    

> 📌 **Regla:** el procediment **no assumeix cap cost d'encuny per defecte**. Si l'encuny és nou, s'ha d'introduir manualment el cost de fabricació com a línia addicional abans de tancar el pressupost.

#### Temps de preparació (setup)

-   **Muntatge de l'encuny a la Heidelberg:** **15 minuts** per comanda (setup únic, ja que només hi ha una passada).
    
-   Si l'encuny és nou, cal afegir el temps de recepció/verificació segons criteri (no inclòs per defecte).
    

#### Fórmula de càlcul (Heidelberg amb encuny)

1.  Etiquetes per full SRA3 (impressió) — igual que al mètode 3.3
    
2.  Fulls SRA3 = sostre(etiquetes\_totals / etiquetes\_per\_full\_SRA3)
    
3.  Subfulls Heidelberg = Fulls SRA3 × 4 (si es divideix en 4 parts)
    
4.  **Passades totals = Subfulls Heidelberg × 1** (passada única amb encuny)
    
5.  Temps troquelat (h) = Passades totals / **1500 fulls/h**
    
6.  Temps preparació (h) = 15 min / 60 = **0,25 h**
    
7.  Temps total (h) = Temps troquelat + Temps preparació
    
8.  Cost troquelat = Temps total × 31,70 €/h
    
9.  **Cost encuny = consultar prèviament** (0 € si és existent; pressupost si és nou)
    
10.  **Cost total tall = Cost troquelat + Cost encuny**
     

#### Exemple pràctic

**Comanda:** 1.000 etiquetes de 25 × 60 mm, encuny existent (cost 0 €)

| Pas | Concepte | Càlcul | Resultat |
| --- | --- | --- | --- |
| 1 | Etq./full SRA3 | 304÷25=12, 434÷60=7 → 12×7 | 84 |
| 2 | Fulls SRA3 | 1000÷84=11,9 → | 12 fulls |
| 3 | Subfulls Heidelberg | 12 × 4 | 48 subfulls |
| 4 | Passades totals | 48 × 1 | 48 passades |
| 5 | Temps troquelat | 48 ÷ 1500 | 0,032 h (1,92 min) |
| 6 | Temps preparació | 15 min | 0,25 h |
| 7 | Temps total | 0,032 + 0,25 | 0,282 h |
| 8 | Cost troquelat | 0,282 × 31,70 € | **8,94 €** |
| 9 | Cost encuny | Existent | **0,00 €** |
| 10 | **Cost total tall** | 8,94 + 0,00 | **8,94 €** |

> Si l'encuny fos nou, caldria sumar el pressupost del proveïdor al pas 9.

---

## 4\. TAULA D'ESCALAT PER A MIG TALL MANUAL

| Etq./full | Temps total (min) | Cost/full (33 €/h) |
| --- | --- | --- |
| 25 | 1,133 | 0,623 € |
| 50 | 1,633 | 0,898 € |
| 75 | 2,033 | 1,118 € |
| 100 | 2,233 | 1,228 € |
| 125 | 2,533 | 1,393 € |
| 150 | 2,833 | 1,558 € |
| 175 | 3,033 | 1,668 € |
| 200 | 3,333 | 1,833 € |
| **250** | **4,233** | **2,328 €** |
| 300 | 4,333 | 2,383 € |
| 400 | 5,333 | 2,933 € |
| 500 | 6,333 | 3,483 € |
| 750 | 8,833 | 4,858 € |
| 1000 | 11,333 | 6,233 € |

**Nota:** Si el nombre d'etiquetes per full no està a la taula, s'usa el **valor immediatament superior**.

---

## 5\. ESTRUCTURA DE COSTOS

| Partida | Càlcul / Base |
| --- | --- |
| **Material** | €/full × nombre de fulls |
| **Impressió** | Cost real per cara (veure taula 5.1) × nombre de fulls × nombre de cares |
| **Preimpressió** | 15 min base (33 €/h) + 5 min/model addicional |
| **Tall** | Guillotinat / Mig tall manual / Heidelberg (2 passades) / Heidelberg amb encuny (1 passada) |
| **Utillatge (encuny)** | **Consultar prèviament. 0 € si és existent; pressupost si és nou** |
| **Empaquetat + transport** | 6 € base + 1,5 min per model (19,93 €/h) |

### 5.1. Costos reals d'impressió (€/cara) — Document de costos operatius 2026

| Concepte | Cost (€/cara) |
| --- | --- |
| **Blanc i negre A4 base** | 0,003147 € |
| **Blanc i negre SRA3 base** | 0,00556 € |
| **Color A4 base** | 0,030426 € |
| **Color SRA3 base** | 0,03966 € |

**Com s'aplica:**

-   El cost és **per cara**. Si s'imprimeix a **1 cara**, s'aplica un cop; si és a **2 cares**, se sumen les dues cares (o es multiplica per 2 si el cost per cara és el mateix).
    
-   El cost s'aplica **per full imprès** (A4 o SRA3 segons el format de sortida). Per a un SRA3 a color 1 cara: `0,03966 € × nombre de fulls SRA3`.
    
-   Per a un A4 a color 1 cara: `0,030426 € × nombre de fulls A4`.
    
-   Aquests costos **substitueixen** l'antic "€/click" i el factor de volum que s'usaven abans. **No s'aplica cap factor de correcció de volum** sobre aquests costos: són costos reals per cara.
    

> ⚠️ **Nota:** si en el futur es volen aplicar factors de volum (per exemple per cobrir costos indirectes en tirades molt petites), s'han d'aplicar **sobre el preu de venda**, no sobre aquests costos reals de producció.

---

## 6\. EXEMPLES PRÀCTICS

### Exemple 1: 800 etiquetes (45×12 mm), mig tall manual, 225/full

| Partida | Càlcul | Import |
| --- | --- | --- |
| Material | 4 fulls × 0,28 € | 1,12 € |
| Impressió | 4 fulls SRA3 × 0,03966 € (color 1 cara) | 0,16 € |
| Preimpressió | 15 min (33 €/h) | 8,25 € |
| Mig tall manual | 4 fulls × 2,328 € (taula 250) | 9,31 € |
| Empaq.+transp. | Fix | 6,00 € |
| **TOTAL** |  | **24,84 €** |

### Exemple 2: 450 etiquetes (80×120 mm), guillotinat, estucat brillant

| Partida | Càlcul | Import |
| --- | --- | --- |
| Material | 45 fulls × 0,2553 € | 11,49 € |
| Impressió | 45 fulls SRA3 × 0,03966 € (color 1 cara) | 1,78 € |
| Preimpressió | 15 min | 8,25 € |
| Guillotinat | 10 min | 4,63 € |
| Empaq.+transp. | Fix | 6,00 € |
| **COST BASE** |  | **32,15 €** |
| Marge 50% |  | 16,08 € |
| **PREU VENDA** |  | **48,23 €** |

### Exemple 3: 1.000 etiquetes (25×60 mm), mig tall Heidelberg, SRA3, 84/full

| Partida | Càlcul | Import |
| --- | --- | --- |
| Material | 12 fulls × 0,28 € (òfset) | 3,36 € |
| Impressió | 12 fulls SRA3 × 0,03966 € (color 1 cara) | 0,48 € |
| Preimpressió | 15 min (33 €/h) | 8,25 € |
| Mig tall Heidelberg | (veure càlcul pas a pas) | 14,73 € |
| Empaq.+transp. | Fix | 6,00 € |
| **TOTAL** |  | **32,82 €** |
| **€/etiqueta** | 32,82 ÷ 1000 | **0,033 €** |

### Exemple 4: 1.000 etiquetes (25×60 mm), mig tall Heidelberg amb encuny existent (1 passada)

| Partida | Càlcul | Import |
| --- | --- | --- |
| Material | 12 fulls × 0,28 € (òfset) | 3,36 € |
| Impressió | 12 fulls SRA3 × 0,03966 € (color 1 cara) | 0,48 € |
| Preimpressió | 15 min (33 €/h) | 8,25 € |
| Mig tall Heidelberg + encuny | (veure càlcul 3.4) | 8,94 € |
| Encuny | Existent (consultat prèviament) | 0,00 € |
| Empaq.+transp. | Fix | 6,00 € |
| **TOTAL** |  | **27,03 €** |
| **€/etiqueta** | 27,03 ÷ 1000 | **0,027 €** |

> **Nota:** si l'encuny fos nou, caldria afegir el pressupost del proveïdor d'utillatge a la línia "Encuny". El cost de tall baixa respecte al mètode de 2 passades (14,73 € → 8,94 €) gràcies a la passada única i la menor preparació, però cal valorar si l'estalvi compensa el cost d'un encuny nou segons el volum de la comanda.

### Exemple 5: 300 fulls DIN A5 (300 unitats finals), adhesiu estucat brillant, color 1 cara, mig tall amb encuny personalitzat existent (1 passada)

-   **Fulls SRA3 necessaris:** 300 A5 ÷ 4 A5 per SRA3 = **75 fulls SRA3**
    
-   **Subfulls A5 a troquelar:** **300**
    

| Partida | Càlcul | Import |
| --- | --- | --- |
| Material | 75 fulls × 0,2553 € | 19,15 € |
| Impressió | 75 fulls SRA3 × 0,03966 € (color 1 cara) | 2,97 € |
| Preimpressió | 15 min (33 €/h) | 8,25 € |
| Troquelat Heidelberg + encuny | 300 passades ÷ 1500 = 0,20 h + 0,25 h setup = 0,45 h × 31,70 € | 14,27 € |
| Encuny | Existent (amortitzat) | 0,00 € |
| Empaq.+transp. | 6 € + 1,5 min (1 model) | 6,50 € |
| **COST DE PRODUCCIÓ** |  | **51,14 €** |
| **€/unitat final (A5)** | 51,14 ÷ 300 | **0,170 €** |

**Proposta de marge (comanda petita, encuny amortitzat):** 100% sobre cost → **102,28 €** (0,341 €/A5). Alternativa competitiva al 75% → **89,50 €** (0,298 €/A5).

---

## 7\. MATERIALS DISPONIBLES (preus / full SRA3)

| Material | Preu / full |
| --- | --- |
| Adhesiu òfset blanc | 0,1915 € |
| Adhesiu estucat brillant | 0,2553 € |
| Adhesiu òfset flúor groc | 0,2780 € |

---

## 8\. NOTES PER A FUTURES COMANDES

-   **Sempre** calcular les dues orientacions de l'etiqueta.
    
-   Per a **mig tall manual**, usar la taula d'escalat.
    
-   Per a **guillotinat**, temps fix de 10 min (més 5 min per model addicional).
    
-   Per a **mig tall amb Heidelberg d'aspes (2 passades)**:
    
    -   Preguntar sempre la mida de troquelat (subfull).
        
    -   SRA3 normalment es divideix en 4 parts.
        
    -   Dues passades per full (horitzontal + vertical).
        
    -   Preparació: 15 + 10 minuts.
        
    -   Velocitat: 2.000 fulls/hora.
        
    -   Cost: 31,70 €/h.
        
-   Per a **mig tall amb Heidelberg d'aspes amb encuny personalitzat (1 passada)**:
    
    -   **Preguntar sempre abans de calcular si l'encuny té cost** (a part dels processos de la feina). Si és existent → 0 €; si és nou → afegir pressupost del proveïdor com a partida pròpia.
        
    -   L'encuny porta tots els talls d'un sol cop: **una sola passada** per troqueladora (no horitzontal + vertical).
        
    -   Velocitat: **1.500 fulls/hora** a mida màxima 350 × 250 mm.
        
    -   Preparació: **15 minuts** (setup únic).
        
    -   Cost hora màquina: 31,70 €/h.
        
    -   Cost total tall = cost troquelat + cost encuny.
        
-   **Impressió:** fer servir sempre els **costos reals per cara** de la taula 5.1 (document de costos operatius 2026). No aplicar factors de volum sobre aquests costos; si cal, aplicar-los sobre el preu de venda.
    
-   Guardar aquest document com a referència per a futures consultes.
    

---

> 📌 **Versió:** 2.3  
> 📅 **Data:** 2027-08-25  
> ✏️ **Elaborat a partir de dades reals de producció**  
> 🔄 **Actualització:** Substituïts els costos d'impressió genèrics (0,06 €/click i factors de volum) pels costos reals per cara del document de costos operatius 2026 (B/N i color, A4 i SRA3). Recalculats tots els exemples amb aquests costos i afegit l'exemple 5 (300 A5 amb encuny existent).
