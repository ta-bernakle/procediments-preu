[PROCEDIMENT: CÀLCUL D'IMPRESSIÓ DE MANUALS FORESTALS A4 COLOR (PLEGAT MANUAL)]
VERSIÓ: 3.1 | DATA: 2026-06-30

1. OBJECTIU
Càlcul de costos per a manuals A4 impresos en color sobre SRA3, amb plegat i grapat MANUAL (4 unitats/minut).

2. ESTRUCTURA FÍSICA DEL PRODUCTE
Un manual A4 es compon de plecs (quaderns) de 2 pàgines A4, que s'imprimeixen a raó de 2 plecs per full SRA3 (un a cada cara).

Per tant:

1 full SRA3 = 2 plecs = 4 pàgines A4 (2 per cara)

Cada plec = 2 pàgines A4 = ½ full SRA3

Exemple per a 16 pàgines totals:

Component	Pàgines	Plecs (2 pàg.)	Fulls SRA3 per unitat
Coberta	2	1	0,5
Interior	14	7	3,5
Total	16	8	4,0
3. MACULATURA (PROVES)
S'afegeix 1 unitat addicional per model per a proves.

S'aplica per separat a cada tipus de paper (interior i coberta).

NO es factura al client.

text
Unitats_producció_tipus = Unitats_client + (Nombre_models × 1)
4. CÀLCUL DE FULLS SRA3 (PER TIPUS DE PAPER)
text
Fulls_SRA3_tipus = Unitats_producció_tipus × (Pàgines_tipus / 4)
On Pàgines_tipus = pàgines A4 d'aquell tipus de paper.

Exemple:

Interior (14 pàgines) → 14/4 = 3,5 fulls/unitat

Coberta (2 pàgines) → 2/4 = 0,5 fulls/unitat

text
Fulls_SRA3_totals = Fulls_SRA3_interior + Fulls_SRA3_coberta
5. COST DE PAPER (PER TIPUS)
text
Cost_paper_tipus = Fulls_SRA3_tipus × (Gramatge_kg × 0,144 × Preu_kg_tipus)
Interior: 1,75 €/kg (estàndard 150 g)

Coberta: 1,90 €/kg (si s'especifica)

6. IMPRESSIÓ
text
Cost_impressió = Fulls_SRA3_totals × 2 × 0,059 €
7. GUILLOTINAT PREVI
text
Temps_guillotinat (min) = MÀXIM(10, 5 + CEILING(Fulls_SRA3_totals / 500) × 3)
Cost_guillotinat = (Temps_guillotinat / 60) × 27,78 €
8. PLECAT I GRAPAT MANUAL
text
Temps_prep_plegat (min) = 10
Temps_prod_plegat (h) = Unitats_producció / 240
Temps_total_plegat (h) = (Temps_prep_plegat / 60) + Temps_prod_plegat
Cost_plegat/grapat = Temps_total_plegat × 39,65 €
text
Cost_grapes = Unitats_producció × 2 × 0,004 €
9. CONSUM ELÈCTRIC + MANTENIMENT
text
Cost_electricitat = Temps_total_plegat × 2,25 × 0,15 €
Cost_manteniment = 2,00 €
10. PREPARACIÓ (IMPOSICIÓ)
text
Cost_preparació = 8,27 € + (Nombre_models - 1) × (4/60 × 33,08 €)
(Nota: 4 minuts = 0,0667 h; 0,0667 × 33,08 = 2,21 € per model addicional)

11. MANIPULAT / EMPAQUETAT
text
Cost_manipulat = (Nombre_models × 5 / 60) × 19,93 €
12. TRANSPORT
text
Cost_transport = 5,00 €
13. MARGE PER DEFECTE (38%)
text
Cost_amb_marge = Cost_total_producció × 1,38
Preu_venda_client = Cost_amb_marge
Preu_per_unitat = Preu_venda_client / Unitats_client
14. TEMPS D'IMPRESSIÓ (ESTIMAT)
text
Temps_impressió (minuts) = (Fulls_SRA3_totals / 1440) × 60
15. EXEMPLE VERIFICAT (model DESBRCAST, 16 pàgines, 200 unitats, 1 model)
Concepte	Fórmula	Resultat
Unitats producció	200 + 1	201
Fulls interior (14 p.)	201 × (14/4)	703,5 → 704
Fulls coberta (2 p.)	201 × (2/4)	100,5 → 101
Total fulls SRA3	704 + 101	805
Cost paper interior	704 × (0,15×0,144×1,75)	26,61 €
Cost paper coberta	101 × (0,25×0,144×1,90)	6,91 €
Cost impressió	805 × 2 × 0,059	94,99 €
Cost guillotinat	(10/60) × 27,78	4,63 €
Cost plegat/grapat	((10/60)+(201/240)) × 39,65	39,80 €
Cost grapes	201 × 2 × 0,004	1,61 €
Electricitat	0,937 × 2,25 × 0,15	0,32 €
Manteniment	fix	2,00 €
Preparació	fix	8,27 €
Manipulat	(1×5/60)×19,93	1,66 €
Transport	fix	5,00 €
TOTAL PRODUCCIÓ		191,80 €
Marge 38%	191,80 × 1,38	264,68 €
Preu per unitat	264,68 / 200	1,32 €

