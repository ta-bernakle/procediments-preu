📄 Procediment d'impressió de bosses i sobres
(Base per a pressupostos i planificació de comandes: bosses, sobres, sobres de finestra, etc.)

⚠️ NOTA IMPORTANT
Aquest procediment ja contempla els canvis proposats al document correctiu
"README — Readaptació de procediments":
- Eliminació del factor de click
- Substitució per cost directe + cost estructural + cost fix + marge
- Marge base per volum i ajust per valor afegit
- Validació amb el mercat
Per tant, és un procediment "corregit i millorat", no un procediment antic pendent de readaptar.

📌 Versió: 1.0 (readaptada)
📅 Data: 2026-10-08
✏️ Elaborat des de zero, a partir del procediment de flyers i del sistema actual de costos
🔄 Pendent: afegir preus de sobres quan estiguin disponibles

---

1. CARACTERÍSTIQUES DEL PRODUCTE
1.1. Bosses
- Material prefabricat: es compren fetes al proveïdor.
- La tira de silicona (si n'hi ha) ja ve incorporada de fàbrica.
- Nosaltres només imprimim, no tallem ni transformem.
- Preu de compra: €/miler o €/unitat (veure COSTOS OPERATIUS.txt → [materials_prefabricats]).
- Mides habituals: 22,9 × 32,4 cm (BF2410), altres mides a consultar.

1.2. Sobres
- Material prefabricat: es compren fets al proveïdor.
- Poden ser blancs, kraft, de color, amb finestra, etc.
- Nosaltres només imprimim, no tallem ni transformem.
- Preu de compra: €/miler o €/unitat (veure COSTOS OPERATIUS.txt → [materials_prefabricats]).
- Mides habituals: 114 × 229 mm, 162 × 229 mm, etc.

1.3. Diferència clau respecte als flyers
- En flyers, el material és paper SRA3 i es calcula per àrea.
- En bosses i sobres, el material és un producte prefabricat i es calcula per unitat.
- No s'aplica guillotinat (no es talla res).
- No s'aplica càlcul d'elements per full SRA3.

---

2. CÀLCUL DEL COST DIRECTE
2.1. Material
material = quantitat × preu_unitari_material

On preu_unitari_material = preu_miler / 1.000

2.2. Impressió
impressio = quantitat × nombre_de_cares × preu_click

On preu_click:
- Color SRA3: 0,0378 €/cara (37,80 €/miler)
- B/N SRA3: 0,0053 €/cara (5,30 €/miler)
- B/N A4: 0,00344 €/cara (3,44 €/miler)

⚠️ NO s'aplica cap factor de multiplicació del cost del click.
El cost del click és el cost real, no s'infla.

2.3. Mà d'obra directa
- Normalment no es desglossa perquè el cost de click ja inclou la impressió.
- Si hi ha manipulació especial, es calcula a part.

2.4. Acabats
- Si el producte ja ve amb l'acabat incorporat (ex: tira de silicona), no es cobra a part.
- Si cal afegir un acabat extra (ex: numeració, segellat), es calcula a part.

Cost directe total = material + impressio + ma_obra_directa + acabats

---

3. CÀLCUL DEL COST ESTRUCTURAL
Cost estructural = Cost directe × Percentatge estructural

El percentatge estructural és el que defineix el sistema actual
(veure SKILL — Càlcul de preus de venda.txt → secció 9).

---

4. CÀLCUL DEL COST FIX
Partida	Base de càlcul
Preimpressió	15 min base × 33,08 €/h + 5 min/model addicional
Preparació de màquines	Segons procediment
Guillotinat	No aplica (producte prefabricat)
Taladrat	No aplica
Empaquetat + transport	6 € base + 1,5 min/model × 19,93 €/h

Cost fix total = preimpressio + preparacio + empaquetat_transport

---

5. COST TOTAL
Cost total = Cost directe + Cost estructural + Cost fix

---

6. MARGE
6.1. Marge base per volum (segons SKILL)
Volum (unitats)	Marge base
≤ 100	100 %
101 – 500	80 %
501 – 2.000	60 %
2.001 – 10.000	50 %
> 10.000	40 %

6.2. Ajust per valor afegit (segons SKILL)
Tipus de feina	Ajust
Simple, estàndard	×1,0
1 acabat o complexitat mitjana	×1,2
2+ acabats o complexitat alta	×1,5
Premium, luxe, personalitzat	×2,0
Urgent (< 48 h)	×1,3
Client nou	×1,1
Client estratègic	×0,9

Marge final = Marge base × Ajust de valor afegit

6.3. Marge mínim garantit
Mai per sota del 30 % sobre cost total, tret de:
- Feines internes
- Feines per a companys
- Feines estratègiques
- Feines de mostra

---

7. PREU DE VENDA
Preu venda = Cost total × (1 + Marge final)

---

8. AJUST PER MOROSITAT INSTITUCIONAL
Els clients institucionals (ajuntaments, consells, etc.) paguen a 90 dies data factura.
Això genera un cost financer ocult que cal compensar.

Càlcul:
- Tipus legal de demora (referència): 10,15 % anual
- Dies de finançament addicional: 60 dies (90 − 30)
- Cost financer = Cost total × 10,15 % × (60 / 365)
- Ajust recomanat: +3 % a +5 % sobre el preu de venda

---

9. EXEMPLE PRÀCTIC
Comanda: 500 bosses blanques Offset Blanco Boltir Eco (BF2410), 1 cara color

Dades:
- Quantitat: 500 bosses
- Material: 68,32 €/miler → 0,06832 €/unitat
- Impressió: 1 cara color → 0,0378 €/cara
- Client: institucional (90 dies)

Càlcul:
Partida	Càlcul	Import
Material	500 × 0,06832	34,16 €
Impressió	500 × 1 × 0,0378	18,90 €
Cost directe		53,06 €
Cost estructural (26 %)	53,06 × 0,26	13,80 €
Cost fix		14,77 €
Cost total		81,63 €
Marge final (80 % × 1,2 = 96 %)	81,63 × 0,96	78,36 €
Preu venda		159,99 €
Ajust morositat (+3 %)		4,80 €
PREU VENDA FINAL		164,79 €
€/bossa		0,33 €

Nota: el preu de 159 € sense ajust de morositat ja és competitiu.
L'ajust de +3 % és opcional si vols cobrir el cost financer.

---

10. NOTES PER A FUTURES COMANDES
- Sempre comprovar si el producte ja té l'acabat incorporat.
- No aplicar guillotinat a bosses ni sobres.
- No aplicar càlcul d'elements per full SRA3.
- Per a color, usar el preu de click color.
- Per a B/N, usar el preu de click B/N.
- Paper de color: demanar preu actualitzat.
- Bosses i sobres de color: demanar preu actualitzat.
- Clients institucionals: considerar ajust per morositat.
- Documentar cada pressupost.
- Guardar aquest document com a referència per a futures consultes.

---

📌 Versió: 1.0 (readaptada)
📅 Data: 2026-10-08
✏️ Elaborat des de zero, a partir del procediment de flyers i del sistema actual de costos
✅ Aquest procediment ja contempla els canvis del document correctiu "README — Readaptació de procediments"
🔄 Pendent: afegir preus de sobres quan estiguin disponibles
