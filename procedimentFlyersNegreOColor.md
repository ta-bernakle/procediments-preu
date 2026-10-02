📄 Procediment d'impressió de fulls (paper normal / estucat)
(Base per a pressupostos i planificació de comandes: flyers, volants, fulls solts, targetes, etc.)
1. FULL ESTÀNDARD
Mida full base: 320 × 450 mm (SRA3 / doble foli)

Vora de seguretat: 8 mm a cada costat

Zona útil: 304 × 434 mm

Altres formats habituals: A4 (foli), A5 (quartilla), A6 (octavilla), targeta, mini

Tall: Guillotinat simple (tall complet, sense mitjos talls ni troquelats)

2. CÀLCUL D'ELEMENTS PER FULL
Per a cada mida d’element, es calculen les dues orientacions i s’escull la que doni més unitats per full.

Fórmula
elements_ample = part_entera(zona_útil_ample / amplada_element)
elements_alt   = part_entera(zona_útil_alt / altura_element)
total_per_full = elements_ample × elements_alt
Exemples
Mida element (mm)	Orientació òptima (ample × alt)	Elements/full SRA3
A6 (105 × 148)	105 × 148	8
A5 (148 × 210)	148 × 210	4
A4 (210 × 297)	210 × 297	2
100 × 150	100 × 150	8
90 × 50	50 × 90	24
210 × 99	210 × 99	6
148 × 105	148 × 105	8
3. IMPRESSIÓ: 1 CARA / 2 CARES, B/N / COLOR
3.1. Tipus d’impressió
Tipus	Descripció	Observacions
1 cara B/N	Només una cara, tinta negra	Cost més baix
2 cares B/N	Dues cares, tinta negra	Cal comptar fulls físics
1 cara color	Una cara, color	Cost per click color
2 cares color	Dues cares, color	Pot ser color a una o dues cares
2 cares mixt	Una cara B/N i una cara color	Cal desglossar costos
3.2. Càlcul de fulls físics
Tipus d’impressió	Fórmula
1 cara	fulls_físics = sostre(unitats_totals / elements_per_full)
2 cares (contingut diferent a cada cara)	fulls_físics = sostre(unitats_totals / (elements_per_full × 2))
2 cares (mateix contingut a les dues cares)	fulls_físics = sostre(unitats_totals / elements_per_full)
4. GUILLOTINAT
4.1. Taula de temps de guillotina per format
Els temps ja inclouen preparació de la guillotina, manipulació, talls, gir de full i canvi de full. No cal afegir res més.

Format	Quantitat base	Temps base (min)	Increment (min/1.000 unitats)	Quan s’aplica
Doble foli (SRA3)	1.000	10	3,96	Fulls SRA3
Foli (A4)	1.000	10	1,96	Fulls A4
Quartilla (A5)	2.000	13	2,04	Fulls A5
Octavilla (A6)	2.000	15	1,89	Fulls A6
Mitja octavilla (targeta)	2.000	20	2,24	Targetes ≥ 85 × 55 mm
Etiqueta mini	2.000	30	2,14	Elements < 85 × 55 mm
4.2. Fórmula
Temps_guillotina (min) = Temps_base + (Quantitat − Quantitat_base) / 1.000 × Increment
Si la quantitat és inferior a la quantitat base → s’agafa el temps base.

Cost_guillotina = Temps_guillotina / 60 × 27,78 €/h
4.3. Exemple
Comanda: 5.000 flyers A5 (quartilla)

Temps = 13 + (5.000 − 2.000) / 1.000 × 2,04
Temps = 13 + 3 × 2,04
Temps = 19,12 min

Cost = 19,12 / 60 × 27,78 = 8,85 €
5. ESTRUCTURA DE COSTOS
Partida	Càlcul / Base
Material	€/full × nombre de fulls
Impressió	€/click × nombre de fulls × factor de volum
Preimpressió	15 min base (33,08 €/h) + 5 min/model addicional
Guillotinat	Taula de temps per format × 27,78 €/h
Empaquetat + transport	6 € base + 1,5 min per model (19,93 €/h)
Factors de correcció d'impressió (PROPOSTA — pendent de validar)
Nota: Aquesta taula és orientativa. Cal validar-la amb casos històrics abans de fixar-la com a definitiva.

Volum (fulls SRA3)	Factor proposat	Justificació
≤ 30	×30	Tirada molt curta, molta preparació per full
31 – 100	×25	Tirada curta
101 – 300	×20	Tirada mitjana-baixa
301 – 600	×18	Tirada mitjana
601 – 1.000	×16	Tirada mitjana-alta
1.001 – 2.000	×15	Tirada alta
2.001 – 5.000	×12	Tirada molt alta
> 5.000	×10	Tirada industrial
Cas de referència: 10.000 flyers A6 B/N 1 cara (1.250 fulls SRA3) → factor ×15 → preu al client 168 € amb marge del 50 %.

6. EXEMPLES PRÀCTICS
Exemple 1: 500 flyers A6 (105×148 mm), 1 cara color, paper estucat
Partida	Càlcul	Import
Material	63 fulls × 0,02898 €	1,83 €
Impressió (×1)	63 × 0,059 €	3,72 €
Preimpressió	15 min (33,08 €/h)	8,27 €
Guillotinat	15 min (base, quantitat < 2.000)	6,95 €
Empaq.+transp.	Fix	6,00 €
TOTAL		26,77 €
€/flyer	26,77 ÷ 500	0,054 €
Exemple 2: 1.000 flyers A5 (148×210 mm), 2 cares color, paper estucat
Partida	Càlcul	Import
Material	125 fulls × 0,02898 €	3,62 €
Impressió (×1)	125 × 0,059 € × 2 cares	14,75 €
Preimpressió	15 min	8,27 €
Guillotinat	13 min (base, quantitat < 2.000)	6,02 €
Empaq.+transp.	Fix	6,00 €
COST BASE		38,66 €
Marge 50%		19,33 €
PREU VENDA		57,99 €
Exemple 3: 10.000 flyers A6 (148,5×105 mm), 1 cara B/N, paper òfset blanc 80 g, factor ×15
Dades de la comanda:

Concepte	Valor
Quantitat	10.000 flyers
Mida	DIN A6 (148,5 × 105 mm)
Impressió	Blanc i negre, 1 cara
Paper	Òfset blanc 80 g
Elements per SRA3	8
Factor click	×15
Preu click B/N	0,003061 €/cara
Càlcul:

Partida	Càlcul	Import
Material	1.250 fulls × 0,02016 €	25,20 €
Impressió (×15)	1.250 × 1 × 0,003061 × 15	57,39 €
Preimpressió	15 min (33,08 €/h)	8,27 €
Guillotinat	30,12 min (taula A6)	13,95 €
Empaq.+transp.	Fix	6,50 €
COST BASE		111,31 €
Marge 50 %		55,66 €
PREU VENDA		166,97 €
€/flyer	166,97 ÷ 10.000	0,0167 €
Nota: Amb factor ×15 i marge del 50 %, el preu al client és 166,97 €, pràcticament els 168 € objectiu. El factor exacte seria ×15,17, però ×15 és prou ajustat per a la proposta.

Exemple 4: 250 targetes (85×55 mm), 2 cares B/N, paper normal
Partida	Càlcul	Import
Material	32 fulls × 0,02016 €	0,65 €
Impressió B/N (×1)	32 × 0,02 € × 2 cares	1,28 €
Preimpressió	15 min (33,08 €/h)	8,27 €
Guillotinat	20 min (base, quantitat < 2.000)	9,26 €
Empaq.+transp.	Fix	6,00 €
TOTAL		25,46 €
€/targeta	25,46 ÷ 250	0,102 €
7. MATERIALS DISPONIBLES (preus / full SRA3)
Material	Gramatge	Cost/full SRA3
Ofset blanc 80 g	80	0,02016 €
Ofset blanc 115 g	115	0,02898 €
Ofset blanc 135 g	135	0,03402 €
Ofset blanc 250 g	250	0,10440 €
Estucat 115 g	115	0,02898 €
Estucat 135 g	135	0,03402 €
Estucat 170 g	170	0,04284 €
Estucat 250 g	250	0,06840 €
Estucat 300 g	300	0,08208 €
Estucat 350 g	350	0,09576 €
Kraftliner 275 g	275	0,05940 €
Nota: Preus calculats a partir de costosOperatius2026.md (€/kg) i l’àrea del full SRA3 (0,144 m²).
Paper de color: no inclòs. Es demana preu en el moment del pressupost perquè fluctua molt.

8. NOTES PER A FUTURES COMANDES
Sempre calcular les dues orientacions de l’element.

Per a 1 cara, el càlcul de fulls és directe.

Per a 2 cares, distingir si el contingut és igual o diferent a cada cara.

Per a color, aplicar el factor de volum corresponent.

Per a B/N, usar el preu de click B/N.

Per a guillotinat, usar la taula de temps per format.

Si la quantitat és inferior a la quantitat base, agafar el temps base.

Si l’element és inferior a 85 × 55 mm, aplicar la taula mini.

Paper de color: demanar preu actualitzat en el moment del pressupost.

Factors de click: la taula actual és una proposta. Cal validar-la amb casos històrics abans de fixar-la.

Guardar aquest document com a referència per a futures consultes.

📌 Versió: 1.0
📅 Data: 2026-10-02
✏️ Elaborat des de zero, a partir del procediment d’etiquetes però sense res d’adhesius ni mig tall
🔄 Pendent: validar la taula de factors de click amb casos històrics
