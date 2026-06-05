# COSTOS OPERATIUS - [EL TEU NEGOCI]
# Versió: 1.0
# Data: 2026-06-05
# Aquest fitxer s'anirà actualitzant amb nous productes i costos

# ============================================================
# 1. PAPER (€/kg)
# ============================================================
# Per gramatge i tipus
[paper]
ofset_80 = 1.75
ofset_115 = 1.75
ofset_135 = 1.75
ofset_250 = 2.90
estucat_115 = 1.75
estucat_135 = 1.75
estucat_170 = 1.75
estucat_250 = 1.90
estucat_300 = 1.90
estucat_350 = 1.90
kraftliner_275 = 1.50

# ============================================================
# 2. IMPRESSIÓ (€/cara)
# ============================================================
[impressio]
b_n_A4_base = 0.003061
color_SRA3_base = 0.059
color_SRA3_custom = 0.046      # per a formats petits (etiquetes)

# ============================================================
# 3. MÀ D'OBRA (€/hora)
# ============================================================
[ma_d_obra]
preparacio_imposicio = 33.08
guillotinat = 27.78
plegat_grapat_extern = 39.65
manipulat_empaquetat = 19.93
foradat = 26.50

# ============================================================
# 4. ENQUADERNACIÓ I ACABATS (€/unitat o €/treball)
# ============================================================
[enquadernacio]
grapa_amortitzada = 0.0065333
grapa_bobina_industrial = 0.004
# espiral_plastico = pendent
# espiral_metal = pendent
# termo_enquadernacio = pendent
# laminat_mate = pendent
# laminat_brillant = pendent

# ============================================================
# 5. COSTOS OPERATIUS INDIRECTES
# ============================================================
[operatius]
electricitat_kWh = 0.15
manteniment_equip_extern = 2.00        # € per treball
transport_per_comanda = 5.00

# ============================================================
# 6. TEMPS ESTÀNDARD (minuts)
# ============================================================
[temps_estandar]
preparacio_document_base = 15
preparacio_model_extra = 5
guillotinat_preparacio_fixa = 5
guillotinat_per_500_full = 3
guillotinat_temps_minim = 10
guillotinat_extra_orientacio_mixta = 3
manipulat_per_model = 5
foradat_velocitat = 150                # etiquetes per minut

# ============================================================
# 7. MACULATURA PER DEFECTE (unitats per model)
# ============================================================
[maculatura]
etiquetes = 6
manuals_color = 4
diplomes = 0
# afegir quan sorgeixin nous productes

# ============================================================
# 8. FORMATS DE MÀQUINA (mm)
# ============================================================
[format_maquina]
SRA3_ample = 320
SRA3_alt = 450
BANNER_ample = 220
BANNER_alt = 660
A3_ample = 297
A3_alt = 420
A4_ample = 297
A4_alt = 210
LUCKY_ample = 262
LUCKY_alt = 350
SRA3PLUS_ample = 330
SRA3PLUS_alt = 488

# ============================================================
# 9. FACTORS MULTIPLICADORS ESPECIALS (per client)
# ============================================================
[factors_especials]
# client_ABC_click_color = 6
# client_XYZ_click_bn = 8

# ============================================================
# 10. NOUS PRODUCTES (a completar quan sorgeixin)
# ============================================================
# Enquadernació espiral:
#   - cost espiral per unitat
#   - temps perforació per unitat
#   - temps muntatge per unitat
#
# Laminat:
#   - cost per m² o per unitat
#   - temps de procés
#
# Troquel:
#   - cost de ferramenta (única)
#   - cost per unitat troquelada
