PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE DESPLEGABLES A5-A3+ (UN SOL FULL) A LA DIGITAL
VERSIÓ: 2.0
DATA: 2026-07-21

1. OBJECTIU
Càlcul de costos per a desplegables impresos en color sobre SRA3, en un sol full (no enquadernats), amb plegat industrial extern i sense grapes.

S'aplica a desplegables amb format final obert (desplegat) des de DIN A5 fins a DIN A3+ (màxim SRA3).

2. NOMENCLATURA
Per evitar confusions, sempre s'ha d'especificar:

Concepte	Definició	Exemple
Mida oberta (desplegada)	Mida final del desplegable quan està completament desplegat	DIN A3
Mida tancada (plegada)	Mida final del desplegable quan està plegat (format de lliurament)	DIN A4
3. ESTRUCTURA FÍSICA DEL PRODUCTE
Un desplegable és un únic full SRA3, imprès a doble cara i plegat posteriorment.

1 desplegable = 1 full SRA3 (2 cares impreses)

Exemples:

Mida oberta	Mida tancada	Fulls SRA3 per unitat
DIN A3	DIN A4	1
DIN A4	DIN A5	1
DIN A5	DIN A6	1
Nota: No hi ha diferenciació entre interior i coberta, ja que és un sol full.

4. DETERMINACIÓ DE DESPLEGABLES PER FULL SRA3
Mida oberta (desplegada)	Dimensions (cm)	Desplegables per SRA3
DIN A3	42,0 × 29,7	1
DIN A4	29,7 × 21,0	2
DIN A5	21,0 × 14,8	4
210 × 297 mm	21,0 × 29,7	2
5. MACULATURA (PROVES)
S'afegeix maculatura per a dos processos:

5.1 Maculatura d'impressora (ajust de color i mides)
text
Maculatura_impressora = 5 fulls SRA3
5.2 Maculatura de plegadora (preparació de la màquina)
Base: 15 unitats en format final obert

La conversió a fulls SRA3 depèn de quants desplegables caben per full:

text
Maculatura_plegadora (SRA3) = CEILING(15 / Desplegables_per_SRA3)
Exemples:

Mida oberta	Desplegables/SRA3	Càlcul	Fulls SRA3
DIN A3	1	15/1 = 15	15
DIN A4	2	15/2 = 7,5	8
DIN A5	4	15/4 = 3,75	4
5.3 Maculatura total
text
Maculatura_total = Maculatura_impressora + Maculatura_plegadora
5.4 Unitats de producció
text
Unitats_producció = Unitats_client + Maculatura_total
Nota: La maculatura NO es factura al client.

6. CÀLCUL DE FULLS SRA3
text
Fulls_SRA3 = Unitats_producció × 1
Exemple: 175 unitats, DIN A3 obert → 175 + 20 = 195 fulls SRA3.

7. COST DE PAPER
Es calcula a partir del gramatge i preu per kg del paper utilitzat (un únic tipus de paper per treball).

text
Cost_paper = Fulls_SRA3 × (Gramatge_kg × 0,144 × Preu_kg)
On:

Gramatge_kg = gramatge en kg/m² (ex: 160 g = 0,160 kg)

0,144 = superfície d'un SRA3 (0,32 m × 0,45 m = 0,144 m²)

Preu_kg = cost del paper per kg (segons proveïdor)

Exemple: 195 fulls, paper 160 g a 1,75 €/kg
→ 195 × (0,160 × 0,144 × 1,75) = 7,86 €

8. IMPRESSIÓ (DIGITAL, DOBLE CARA, COLOR)
8.1 Determinació del factor multiplicador
El cost del click de color s'escala segons el volum d'impressions SRA3:

Volum (impressions SRA3)	Factor multiplicador
Fins a 250	6×
De 251 a 500	4×
De 501 a 1.000	3×
Nota: El volum es calcula sobre Fulls_SRA3 (no sobre cares). Una impressió SRA3 = 1 full.

8.2 Càlcul del cost d'impressió
text
Cost_per_cara_base = 0,059 €
Cost_per_cara_amb_factor = 0,059 × Factor_multiplicador
Cost_impressió = Fulls_SRA3 × 2 × Cost_per_cara_amb_factor
Exemple (195 fulls, ≤250):

Factor = 6×

Cost per cara = 0,059 × 6 = 0,354 €

Cost impressió = 195 × 2 × 0,354 = 138,06 €

9. GUILLOTINAT PREVI AL PLECAT
Tall previ per ajustar el SRA3 a la mida necessària abans del plegat.

text
Temps_guillotinat (min) = MÀXIM(10, 5 + CEILING(Fulls_SRA3 / 500) × 3)
Cost_guillotinat = (Temps_guillotinat / 60) × 27,78 €
Exemple (195 fulls):

CEILING(195/500) = 1

Temps = 5 + 1×3 = 8 → MÀXIM(10, 8) = 10 min

Cost = (10/60) × 27,78 = 4,63 €

10. PLECAT INDUSTRIAL (EXTERN)
S'utilitza plegadora industrial externa amb els següents paràmetres:

Preu/hora: 39,65 €

Preparació màquina: 15 minuts (0,25 h)

Rendiment: 6.000 fulls/hora (promig)

text
Temps_prep_plegat = 15 / 60 = 0,25 h
Temps_prod_plegat = Fulls_SRA3 / 6000  (en hores)
Temps_total_plegat = Temps_prep_plegat + Temps_prod_plegat
Cost_plegat = Temps_total_plegat × 39,65 €
Exemple (195 fulls):

Preparació: 0,25 h

Producció: 195/6000 = 0,0325 h

Total: 0,2825 h

Cost: 0,2825 × 39,65 = 11,20 €

11. FENDIT (SI GRAMATGE > 170 g O PAPER ESTUCAT)
En cas de gramatges superiors a 170 g (especialment en papers estucats), cal afegir un fendit previ al plegat per evitar esquerdaments a les vores del plec.

Paràmetres:

Preu/hora: 31,70 €

Preparació màquina: 10 minuts (0,1667 h)

Rendiment variable segons llargada del full (en direcció d'alimentació):

Llargada del full	Rendiment (peces/hora)
≥ 42 cm (SRA3 apaïsat)	1.200
< 42 cm (SRA3 vertical o més petit)	1.700
text
Si gramatge > 170 g O paper estucat = TRUE:
    Temps_prep_fendit = 10 / 60 = 0,1667 h
    Si llargada_full >= 42 cm:
        Temps_prod_fendit = Fulls_SRA3 / 1200
    Sinó:
        Temps_prod_fendit = Fulls_SRA3 / 1700
    
    Temps_total_fendit = Temps_prep_fendit + Temps_prod_fendit
    Cost_fendit = Temps_total_fendit × 31,70 €
Sinó:
    Cost_fendit = 0 €
Exemple (195 fulls, SRA3 vertical <42 cm, paper estucat 200 g):

Preparació: 0,1667 h

Producció: 195/1700 = 0,1147 h

Total: 0,2814 h

Cost: 0,2814 × 31,70 = 8,92 €

12. PREPARACIÓ / IMPOSICIÓ
text
Cost_preparació = 8,27 € + (Nombre_models - 1) × (4/60 × 33,08 €)
(4 minuts = 0,0667 h; 0,0667 × 33,08 = 2,21 € per model addicional)

Exemple (1 model): 8,27 €

13. EMPAQUETAT / MANIPULAT
text
Cost_manipulat = (Nombre_models × 5 / 60) × 19,93 €
Exemple (1 model): (5/60) × 19,93 = 1,66 €

14. TRANSPORT
text
Cost_transport = 5,00 €
15. MARGE PER DEFECTE (50%)
text
Cost_total_producció = Cost_paper + Cost_impressió + Cost_guillotinat + Cost_plegat + Cost_fendit + Cost_preparació + Cost_manipulat + Cost_transport
Cost_amb_marge = Cost_total_producció × 1,50
Preu_venda_client = Cost_amb_marge
Preu_per_unitat = Preu_venda_client / Unitats_client
16. TEMPS D'IMPRESSIÓ (ESTIMAT)
text
Temps_impressió (minuts) = (Fulls_SRA3 / 1440) × 60
Exemple (195 fulls): (195/1440)×60 = 8,13 minuts

17. EXEMPLE VERIFICAT (ESTÀNDARD)
Dades d'entrada:
Paràmetre	Valor
Producte	Díptic DIN A3 obert / A4 tancat
Unitats	175
Models	1
Paper	Òfset blanc 160 g
Preu paper	1,75 €/kg
Impressió	Color, doble cara
Plegat	Díptic simple (1 plec)
Fendit	NO (160 g < 170 g)
Maculatura impressora	5 fulls SRA3
Maculatura plegadora	15 fulls SRA3 (DIN A3 = 1/SRA3)
Factor click	6× (≤250 impressions)
Marge	50%
Càlculs:
Concepte	Fórmula	Resultat
Maculatura total	5 + 15	20 fulls
Unitats producció	175 + 20	195
Fulls SRA3	195 × 1	195
Cost paper	195 × (0,160×0,144×1,75)	7,86 €
Cost impressió	195 × 2 × (0,059×6)	138,06 €
Cost guillotinat	(10/60) × 27,78	4,63 €
Cost plegat	(0,25 + 195/6000) × 39,65	11,20 €
Cost fendit	No aplica	0,00 €
Preparació	fix	8,27 €
Manipulat	(1×5/60)×19,93	1,66 €
Transport	fix	5,00 €
TOTAL PRODUCCIÓ		176,68 €
Marge 50%	176,68 × 1,50	265,02 €
Preu per unitat	265,02 / 175	1,51 €
18. TAULA DE MACULATURA DE PLECADORA (REFERÈNCIA RÀPIDA)
Desplegables per SRA3	Càlcul	Fulls SRA3 (arrodonit)
1 (DIN A3)	15 / 1 = 15	15
2 (DIN A4)	15 / 2 = 7,5	8
3	15 / 3 = 5	5
4 (DIN A5)	15 / 4 = 3,75	4
6	15 / 6 = 2,5	3
8	15 / 8 = 1,875	2
9+	15 / n < 2	2 (mínim 2 per ajustos)
19. OBSERVACIONS FINALS
Sense grapes (no s'aplica cost de grapes ni grapat manual).

Un sol tipus de paper per treball (no hi ha coberta/interior diferenciats).

El fendit només s'aplica si el gramatge supera 170 g o el paper és estucat.

La llargada del full per al càlcul del fendit es refereix a la direcció d'alimentació de la plegadora.

El factor multiplicador del click s'aplica segons el volum total de fulls SRA3.

La maculatura NO es factura al client.

FI DEL PROCEDIMENT
Guardat com a ProcedimentDesplegablesA5-A3+.md
