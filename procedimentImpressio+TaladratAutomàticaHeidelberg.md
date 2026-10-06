📄 Procediment de fulls taladrats a Heidelberg d’aspes
(Base per a pressupostos i planificació de comandes)

1. DESCRIPCIÓ GENERAL
Aquest procediment cobreix fulls impresos en paper normal (estàndard o extra) que després es taladren a la màquina automàtica d’aspes Heidelberg i finalment es guillotinen a la mida final.

Característiques habituals:

Taladrat simple: 1 sol trepat (o patró de trepats) que parteix el full en dues meitats o separa matriu i còpia.

Paper: òfset estàndard o extra (amb el petit increment de cost que comporta).

Impressió: 1 o 2 cares, color o blanc i negre.

Guillotinat: tall complet simple, segons la mida final indicada pel client.

Diversos formats dins el SRA3: possible, i caldrà definir com es parteix el full per taladrar.

2. FULL ESTÀNDARD
Mida full base: 320 × 450 mm (SRA3 / doble foli)

Vora de seguretat: 4 mm a cada costat

Zona útil: 304 × 434 mm

Tall: Guillotinat simple (sense mitjos talls ni troquelats complexos)

3. CÀLCUL D’ELEMENTS PER FULL
Per a cada mida d’element, es calculen les dues orientacions i s’escull la que doni més unitats per full.

Fórmula:

elements_ample = part_entera(zona_útil_ample / amplada_element)
elements_alt   = part_entera(zona_útil_alt / altura_element)
total_per_full = elements_ample × elements_alt

Exemples:
Mida element (mm)	Orientació òptima	Elements/full SRA3
A4 (210 × 297)	297 × 210	2
A5 (148 × 210)	148 × 210	4
A6 (105 × 148)	105 × 148	8
26 × 26 cm	260 × 260	1
43 × 20 cm	200 × 430	1
26 × 15 cm	260 × 150	2

4. IMPRESSIÓ: 1 CARA / 2 CARES, B/N / COLOR

4.1. Tipus d’impressió
Tipus	Descripció	Observacions
1 cara B/N	Només una cara, tinta negra	Cost més baix
2 cares B/N	Dues cares, tinta negra	Cal comptar fulls físics
1 cara color	Una cara, color	Cost per click color
2 cares color	Dues cares, color	Pot ser color a una o dues cares
2 cares mixt	Una cara B/N i una cara color	Cal desglossar costos

4.2. Càlcul de fulls físics
Tipus d’impressió	Fórmula
1 cara	fulls_físics = sostre(unitats_totals / elements_per_full)
2 cares (contingut diferent a cada cara)	fulls_físics = sostre(unitats_totals / (elements_per_full × 2))
2 cares (mateix contingut a les dues cares)	fulls_físics = sostce(unitats_totals / elements_per_full)

5. TALADRAT A HEIDELBERG D’ASPES

5.1. Descripció de la màquina
Màquina: Heidelberg d’aspes (full a full, en pla)

Format màxim del full: 250 × 350 mm

Format promig de treball: 160 × 225 mm (1/4 de SRA3)

Velocitat de treball: 2.500 fulls/hora (format promig)

Cost hora màquina: 31,70 €/h

5.2. Tipus de taladrat
Tipus	Passades	Observacions
Taladrat simple	1 passada	1 sol trepat o patró de trepats
Taladrat doble	2 passades	Horitzontal + vertical (com al mig tall d’etiquetes)
En aquest procediment, el cas habitual és el taladrat simple (1 passada).

5.3. Preparació (setup)
Concepte	Temps
Preparació base	15 min
Preparació addicional (si cal canvi de motlle)	10 min
Total preparació habitual: 15 min = 0,25 h

5.4. Velocitat
Format subfull	Velocitat
Format promig (160 × 225 mm)	2.500 fulls/hora
Formats més grans	Cal ajustar (més lent)
Formats més petits	Cal ajustar (més ràpid)
Nota: Si el format és superior a 225 × 320 mm, la velocitat pot baixar. Si és inferior, pot pujar. Cal validar-ho amb casos reals.

5.5. Fórmula de càlcul

1. Subfulls Heidelberg = Fulls SRA3 × (nombre de divisions)
2. Passades totals = Subfulls Heidelberg × nombre de passades
3. Temps taladrat (h) = Passades totals / Velocitat (fulls/h)
4. Temps preparació (h) = 15 min / 60 = 0,25 h
5. Temps total (h) = Temps taladrat + Temps preparació
6. Cost taladrat = Temps total × 31,70 €/h

5.6. Exemple pràctic
Comanda: 2.000 fulls A4, taladrat simple, 1 passada, 2.500 fulls/h

Pas	Concepte	Càlcul	Resultat
1	Subfulls Heidelberg	2.000 SRA3 × 1 divisió	2.000 subfulls
2	Passades totals	2.000 × 1	2.000 passades
3	Temps taladrat	2.000 / 2.500	0,8 h (48 min)
4	Temps preparació	15 min	0,25 h
5	Temps total	0,8 + 0,25	1,05 h
6	Cost taladrat	1,05 × 31,70	33,29 €

6. GUILLOTINAT

6.1. Taula de temps de guillotina per format
Els temps ja inclouen preparació de la guillotina, manipulació, talls, gir de full i canvi de full. No cal afegir res més.

Format	Quantitat base	Temps base (min)	Increment (min/1.000 unitats)	Quan s’aplica
Doble foli (SRA3)	1.000	10	3,96	Fulls SRA3
Foli (A4)	1.000	10	1,96	Fulls A4
Quartilla (A5)	2.000	13	2,04	Fulls A5
Octavilla (A6)	2.000	15	1,89	Fulls A6
Mitja octavilla (targeta)	2.000	20	2,24	Targetes ≥ 85 × 55 mm
Etiqueta mini	2.000	30	2,14	Elements < 85 × 55 mm

6.2. Fórmula
Temps_guillotina (min) = Temps_base + (Quantitat − Quantitat_base) / 1.000 × Increment
Si la quantitat és inferior a la quantitat base → s’agafa el temps base.
Cost_guillotina = Temps_guillotina / 60 × 27,78 €/h

6.3. Guillotinat addicional
Si cal dividir el full SRA3 abans del taladrat (guillotinat intermig):
Temps addicional: 5 min

Cost: 5 / 60 × 27,78 = 2,32 €

7. ESTRUCTURA DE COSTOS
Partida	Càlcul / Base
Material	€/full × nombre de fulls
Impressió	€/click × nombre de fulls × factor de volum
Preimpressió	15 min base (33,08 €/h) + 5 min/model addicional
Guillotinat	Taula de temps per format × 27,78 €/h
Taladrat Heidelberg	Temps total × 31,70 €/h
Empaquetat + transport	6 € base + 1,5 min per model (19,93 €/h)
Factors de correcció d’impressió (PROPOSTA — pendent de validar)
Volum (fulls SRA3)	Factor proposat
≤ 30	×30
31 – 100	×25
101 – 300	×20
301 – 600	×18
601 – 1.000	×16
1.001 – 2.000	×15
2.001 – 5.000	×12
> 5.000	×10
⚠️ Atenció: Aquesta taula és una proposta. Per a fulls taladrats, el factor sol ser molt més baix (entre 1 i 1,5), com s’ha vist al cas de 2.000 fulls A4. Cal validar-la amb casos reals abans de fixar-la.

8. EXEMPLE PRÀCTIC
2.000 fulls A4, color 1 cara, òfset extra 90 g, taladrat simple, factor 1,3
Dades:

Concepte	Valor
Quantitat	2.000 fulls A4
Impressió	Color, 1 cara
Paper	Òfset extra 90 g
Elements per SRA3	2
Fulls SRA3	1.000
Factor click	1,3
Taladrat	Simple, 1 passada, 2.500 fulls/h, 15 min preparació
Càlcul:

Partida	Càlcul	Import
Material	1.000 × 0,02704 €	27,04 €
Impressió (×1,3)	1.000 × 1 × 0,059 × 1,3	76,70 €
Preimpressió	15 min (33,08 €/h)	8,27 €
Guillotinat	16,96 min (A4 + untermig)	7,85 €
Taladrat Heidelberg	1,05 h × 31,70 €/h	33,29 €
Empaquetat + transport	Fix	6,50 €
COST BASE		159,65 €
Marge 50 %		79,83 €
PREU VENDA		239,48 €
€/miler	239,48 ÷ 2	119,74 €
Comparativa 2025: 112,16 €/miler → +6,76 %

9. NOTES PER A FUTURES COMANDES
Sempre calcular les dues orientacions de l’element.

Per a 1 cara, el càlcul de fulls és directe.

Per a 2 cares, distingir si el contingut és igual o diferent a cada cara.

Per a color, aplicar el factor de volum corresponent.

Per a B/N, usar el preu de click B/N.

Per a guillotinat, usar la taula de temps per format.

Per a taladrat Heidelberg, usar la fórmula de la secció 5.5.

Si cal dividir el full SRA3 abans del taladrat, afegir 5 min de guillotinat.

Si l’element és inferior a 85 × 55 mm, aplicar la taula mini.

Paper de color: demanar preu actualitzat en el moment del pressupost.

Òfset extra: aplicar regla de tres + 6 % sobre el preu de l’òfset estàndard.

Factors de click: la taula actual és una proposta. Per a fulls taladrats, el factor sol ser proper a 1.

Guardar aquest document com a referència per a futures consultes.

📌 Versió: 1.0
📅 Data: 2026-10-06
✏️ Elaborat a partir del procediment d’impressió de fulls, afegint el taladrat Heidelberg
🔄 Pendent: validar la taula de factors de click amb casos històrics


